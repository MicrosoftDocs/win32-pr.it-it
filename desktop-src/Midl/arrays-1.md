---
title: Arrays (attributo)
description: Le matrici sono raccolte omogenee di dati a cui si accede tramite un indice o un numero di elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- Arrays attribute MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299097"
---
# <a name="arrays-attribute"></a>Arrays (attributo)

Le matrici sono raccolte omogenee di dati a cui si accede tramite un indice o un numero di elemento.

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo-attr-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano al tipo. Gli attributi di tipo validi includono [**\[ \] handle**](handle.md), [**\[ \_ \] tipo di commutione**](switch-type.md), [**\[ trasmissione \_ come \]**](transmit-as.md); [**\[ riferimento \]**](ref.md)all'attributo del puntatore, [**\[ univoco \]**](unique.md)o [**\[ ptr \]**](ptr.md)e l' [**\[ \_ handle \] di contesto**](context-handle.md), la [**\[ stringa \]**](string.md)e l' [**\[ Ignore \]**](ignore.md)degli attributi di utilizzo. Separare più attributi con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica l'identificatore del tipo, il tipo di base, lo [**struct**](struct.md), l' [**Unione**](union.md)o il tipo [**enum**](enum.md) . La specifica del tipo può includere una specifica di archiviazione facoltativa.

</dd> <dt>

*puntatore-decl* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è lo stesso del dichiaratore del puntatore utilizzato in C, costruito dall' **\*** indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*dichiaratore di matrici* 
</dt> <dd>

Specifica il nome della matrice, seguito da uno dei costrutti seguenti per ogni dimensione della matrice: "**\[ \]**", " **\[\*\]** ", "**\[ ***Cost1*** \]**" o "**\[ ***lower...*** Upper \]**"dove *Lower* e *Upper* sono valori costanti che rappresentano i limiti inferiore e superiore. La costante *inferiore* deve restituire zero.

</dd> <dt>

*tag* 
</dt> <dd>

Specifica un tag facoltativo per la struttura o l'Unione.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano alla struttura, al membro dell'Unione o al parametro della funzione. Gli attributi di campo validi includono [**\[ First \_ è \]**](first-is.md), [**\[ Last \_ è \]**](last-is.md), [**\[ length \_ \] is**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md); the usage Attributes [**\[ String \]**](string.md), and [**\[ Ignore \]**](ignore.md); The Pointer Attributes [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md), [**\[ ptr \]**](ptr.md)e The Union Attribute [**\[ Switch \_ Type \]**](switch-type.md). Separare più attributi di campo con virgole. Si noti che gli attributi elencati sopra, **\[ First \_ \]** sono, **\[ Last \_ is \]** e [**\[ Ignore \]**](ignore.md) non sono validi per le unioni.

</dd> <dt>

*espressione limitata* 
</dt> <dd>

Specifica un'espressione del linguaggio C. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono [**\[ \] callback**](callback.md), [**\[ \] local**](local.md), l'attributo Pointer [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md)e la [**\[ stringa \]**](string.md)degli attributi di utilizzo e l' [**\[ \_ handle \] di contesto**](context-handle.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*param-attr-List* 
</dt> <dd>

Specifica gli attributi direzionali e uno o più attributi di campo facoltativi che si applicano al parametro di matrice. Gli attributi di campo validi includono [**\[ Max \_ è \]**](max-is.md), [**\[ size \_ \] è**](size-is.md), [**\[ length \_ è \]**](length-is.md), [**\[ First \_ è \]**](first-is.md)e [**\[ Last \_ è \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le matrici in MIDL usano uno stile simile a, ma non esattamente come C e C++. Per altre informazioni, vedere [matrici MIDL](midl-arrays.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**callback**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[**gestire**](handle.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
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

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 




