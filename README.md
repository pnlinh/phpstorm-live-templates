Подробнее с шаблонами можно познакомиться [здесь](https://www.jetbrains.com/help/phpstorm/2016.1/live-templates.html).
Все шаблоны предназначены для php и yii2. В качестве аббревиатуры выступает заголовок.

- [Шаблоны для всех областей применения](#Шаблоны-для-всех-областей-применения)
    - [Typograpghy | Double-angle quotation mark | ("")](#Шаблоны-для-всех-областей-применения)
    - [Typograpghy | Emdash (Long dash) | (--)](#--)
- [Шаблоны Bootstrap и тем](Шаблоны-bootstrap-и-тем)
    - [Boostrap | Widget tags | (widget)](#widget)
- [HTML шаблоны](#html-шаблоны)
    - [PHP | Echo php code | (=)](#-1)
    - [PHP | Echo php code | (ec)](#ec)
    - [YII2 | Translation of word via Yii:t() | (yt)](#yt)
    - [YII2 | Url helper | (url)](#url)
    - [YII2 | Url helper | (uweb)](#uweb)
    - [YII2 | Url helper | (route)](#route)
    - [PHP | Open php tag | (php)](#php)
    - [PHP | Number Format | (nf)](#nf)
    - [PHP | Generates/surrounds selection with foreach | (foreach)](#foreach)
    - [PHP | Generates/surrounds selection with if | (if)](#if)
    - [PHPDoc | Generates PHP comment block with @var | (var)](#var)
    - [PHP | Generates/surronds selection with php comment | (cmt)](#cmt)
- [PHP шаблоны](#php-шаблоны)
    - [Yii2 | Register Meta-tags | (rmt)](#rmt)
    - [Yii2 | DB transaction | (yiitrans)](#yiitrans)
    - [Yii2 | Controller action | (act)](#act)

## Шаблоны для всех областей применения


### "" 
```
«$SELECTION$»
```
Typograpghy | Double-angle quotation mark

### --
```
—
```
Typograpghy | Emdash (Long dash)

## Шаблоны Bootstrap и тем

### widget
```html
<div class="widget">
    <div class="widget-content padding">
        $SELECTION$
    </div>
</div>
```
Bootstrap | Widget tags

## HTML шаблоны

### =
```php
<?= $END$ ?>
```
PHP | Echo php code.

### ec
```php
<?= $END$ ?>
```
PHP | Echo php code.

### yt
```php
<?= Yii::t('frontend', '$SELECTION$') ?>
```
YII2 | Translation of word via Yii:t()

### url
```php
<?= Url::to('$SELECTION$') ?>
```
YII2 | Url helper

### uweb
```php
<?= Url::to('@web/$END$') ?>
```
YII2 | Url helper

### route
```php
<?= Url::to(['$END$']) ?>
```
YII2 | Url helper

### php
```php
<?php $END$ ?>
```
PHP | Open php tag

### nf
```php
<?= number_format($VAR$, 0, ',', ' ') ?>
```
PHP | Number Format

### foreach
```php
<?php foreach($ARRAY$ as $KEY$ => $VALUE$): ?>
    $SELECTION$
<?php endforeach ?>
```
PHP | Generates/surrounds selection with foreach

### if
```php
<?php if ($CONDITION$) : ?>
    $SELECTION$
<?php endif; ?>
```
PHP | Generates/surrounds selection with if

### var
```php
<?php
/**
 * @var $END$
 */
?>
```
PHPDoc | Generates PHP comment block with @var

### cmt
```php
<?php /*
$SELECTION$
*/ ?>
```
PHP | Generates/surronds selection with php comment

## PHP шаблоны

### rmt
```php
$this->registerMetaTag([
    'name' => '$TAGNAME$',
    'content' => $SELECTION$,
]);
```
Yii2 | Register Meta-tags

### yiitrans
```php
$transaction = Yii::$app->db->beginTransaction();
try {
    $END$
    $transaction->commit();
} catch (\Exception $e) {
    $transaction->rollBack();
}
```

Yii2 | DB transaction

### act
```php
public function action$NAME$($PARAMETERS$)
{
    return $END$;
}
```

Yii2 | Controller action

