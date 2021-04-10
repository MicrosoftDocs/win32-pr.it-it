---
title: switch_is (attributo)
description: Il parametro \ Switch \_ is \ attribute specifica l'espressione o l'identificatore che funge da discriminante di Unione che seleziona il membro di Unione.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- attributo switch_is MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955976"
---
# <a name="switch_is-attribute"></a>Switch \_ è attributo

L' **\[ opzione \_ è \]** attribute specifica l'espressione o l'identificatore che funge da discriminante di Unione che seleziona il membro di Unione.

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

*struct-Tag* 
</dt> <dd>

Specifica un tag facoltativo per una struttura.

</dd> <dt>

*Limited-expr* 
</dt> <dd>

Specifica un'espressione del linguaggio C supportata da MIDL. Sono supportate quasi tutte le espressioni in linguaggio C. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di pre-e post-incremento e di pre-e post-decremento.

</dd> <dt>

*Field-attr-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano a un membro di Unione. Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e per i membri che sono a loro volta Unions, il **\[** [**\_ tipo di opzione**](switch-type.md)dell'attributo Union **\]** . Separare più attributi di campo con virgole.

</dd> <dt>

*Union-Type-specifier* 
</dt> <dd>

Specifica l'identificatore del tipo di [**Unione**](union.md) . Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*dichiaratore e declarator-list* 
</dt> <dd>

Specifica un dichiaratore C standard, ad esempio un identificatore, un dichiaratore di puntatore e un dichiaratore di matrice. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle unioni trasmesse in chiamate a procedure remote. Questi dichiaratori sono consentiti nelle unioni non trasmesse. Separare più dichiaratori con virgole.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** , l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e gli attributi Usage **\[ String \]**, **\[ Ignore \]** e **\[ Context \_ handle \]**.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' [**Unione**](union.md), un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*puntatore-dichiaratore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*param-attr-List* 
</dt> <dd>

Specifica zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi **\[ di \]** parametro possono attivare e **\[ \]** disattivare gli attributi direzionali, gli attributi di campo **\[ First \_ \]** sono, **\[ Last \_ \] è**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ size \_ is \]** e **\[ Switch \_ Type \]**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi Usage. L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> <dt>

*tipo Unione* 
</dt> <dd>

Identifica l'identificatore del tipo di [**Unione**](union.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il discriminante associato all' **\[ opzione \_ è \]** l'attributo deve essere definito allo stesso livello logico dell'Unione:

-   Quando l'Unione è un parametro, il discriminante di Unione deve essere un altro parametro.
-   Quando l'Unione è un campo di una struttura, discriminante deve essere un altro campo della stessa struttura.

La sequenza in una struttura o in un elenco di parametri di funzione non è significativa. L'Unione può precedere o seguire discriminante.

L' **\[ opzione \_ è \]** attributo può essere visualizzata come attributo di campo o come attributo di parametro.

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

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[Unioni incapsulate](encapsulated-unions.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[Unioni non incapsulate](nonencapsulated-unions.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 




