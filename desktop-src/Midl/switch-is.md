---
title: switch_is (attributo)
description: L'attributo \ switch is\ specifica l'espressione o l'identificatore che funge da discriminante dell'unione che \_ seleziona il membro di unione.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is attributo MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1975dcf38a04fc127de199e7cc663c8af41b63e6ce8f92d38be2115316ed0727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382842"
---
# <a name="switch_is-attribute"></a>\_l'opzione è l'attributo

**\[ \_ L'opzione \] è** l'attributo che specifica l'espressione o l'identificatore che funge da discriminante dell'unione che seleziona il membro dell'unione.

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*struct-tag* 
</dt> <dd>

Specifica un tag facoltativo per una struttura .

</dd> <dt>

*limited-expr* 
</dt> <dd>

Specifica un'espressione in linguaggio C supportata da MIDL. Quasi tutte le espressioni in linguaggio C sono supportate. Il compilatore MIDL supporta espressioni condizionali, espressioni logiche, espressioni relazionali ed espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori pre e post-incremento e pre-decremento.

</dd> <dt>

*field-attr-list* 
</dt> <dd>

Specifica zero o più attributi di campo applicabili a un membro di unione. Gli attributi di campo validi includono first è , last è , length è , max è , size è ; la stringa degli attributi di utilizzo , ignore e context handle ; l'attributo **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [**puntatore ref**](ref.md), **\]** unique o ptr ; **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](switch-type.md) **\]** e per i membri che sono unioni, il tipo di opzione dell'attributo union . Separare più attributi di campo con virgole.

</dd> <dt>

*union-type-specifier* 
</dt> <dd>

Specifica l'identificatore [**del tipo**](union.md) di unione. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*declarator e declarator-list* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore e un dichiaratore di matrice. I dichiaratori di funzione e le dichiarazioni di campo di bit non sono consentiti nelle unioni trasmesse nelle chiamate di procedura remota. Questi dichiaratori sono consentiti nelle unioni che non vengono trasmesse. Separare più dichiaratori con virgole.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono callback , local ; l'attributo **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ puntatore ref \]**, **\[ unique \]** o **\[ ptr \]** e **\[ \]** **\[ \]** **\[ \_ \]** gli attributi di utilizzo string , ignore e context handle .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Specifica un tipo [di base,](midl-base-types.md) [**uno struct,**](struct.md) [**un'unione,**](union.md) [**un tipo enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *type-specifier*.

</dd> <dt>

*dichiaratore di puntatore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è lo stesso del dichiaratore di puntatore usato in C; viene costruito dal \* designatore, dai modificatori come **far** e dal qualificatore [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*param-attr-list* 
</dt> <dd>

Specifica zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi dei parametri possono assumere gli attributi direzionali **\[ \] in** e **\[ \] out**, **\[ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** gli attributi del campo sono , **\[ \_ \]** last è , length è , max è , size è e switch type ; l'attributo **\[ puntatore ref \]**, unique o **\[ ptr \]** e l'handle **\[ \_ \]** di contesto degli attributi di utilizzo e string . L'attributo **\[ di utilizzo ignore \]** non può essere usato come attributo di parametro. Separare più attributi con virgole.

</dd> <dt>

*union-type* 
</dt> <dd>

Identifica [**l'identificatore del**](union.md) tipo di unione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La discriminante associata **\[ all'opzione \_ è \]** l'attributo deve essere definito allo stesso livello logico dell'unione:

-   Quando l'unione è un parametro, l'unione discriminante deve essere un altro parametro.
-   Quando l'unione è un campo di una struttura, il discriminante deve essere un altro campo della stessa struttura.

La sequenza in una struttura o in un elenco di parametri di funzione non è significativa. L'unione può precedere o seguire la discriminante.

**\[ \_ L'opzione \] è** attribute può essere visualizzata come attributo di campo o come attributo di parametro.

## <a name="examples"></a>Esempi

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**callback**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[Unioni incapsulate](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**il \_ primo è**](first-is.md)
</dt> <dt>

[**Ignorare**](ignore.md)
</dt> <dt>

[**\_l'ultimo è**](last-is.md)
</dt> <dt>

[**length \_ è**](length-is.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**max \_ è**](max-is.md)
</dt> <dt>

[Unioni non incapsulate](nonencapsulated-unions.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**size \_ è**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**tipo di \_ commutatore**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> </dl>

 

 




