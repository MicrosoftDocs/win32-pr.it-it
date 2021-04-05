---
title: in (attributo)
description: L'attributo \ in \ indica che un parametro deve essere passato dalla routine chiamante alla routine chiamata.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- in attributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726967"
---
# <a name="in-attribute"></a>in (attributo)

L'attributo **\[ in \]** indica che un parametro deve essere passato dalla routine chiamante alla routine chiamata.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Function-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione. Gli attributi di funzione validi sono **\[ callback \]**, **\[ \] local**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** e la **\[ stringa \]** degli attributi Usage, **\[ Ignore \]** e **\[ \_ handle \] di contesto**.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un **\_ tipo di base**, uno [**struct**](struct.md), un' [**unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*puntatore-dichiaratore* 
</dt> <dd>

Specifica zero o più dichiaratori di puntatore. Un dichiaratore di puntatore è uguale al dichiaratore del puntatore utilizzato in C; viene costruita dall' \* indicatore, i modificatori, ad esempio **lontano**, e il qualificatore [**const**](const.md).

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della procedura remota.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi appropriati per il tipo di parametro specificato. Gli attributi di parametro con l'attributo in possono anche prendere l'attributo direzionale **\[ \] out**; gli attributi **\[ \] di** campo **\[ First \_ sono \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ size \_ is \]** e **\[ Switch \_ Type \]**, l'attributo Pointer **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]**; e l' **\[ \_ handle \]** e la **\[ stringa \]** del contesto degli attributi Usage. L'attributo Usage **\[ Ignore \]** non può essere utilizzato come attributo di parametro. Separare più attributi con virgole.

</dd> <dt>

*dichiaratore* 
</dt> <dd>

Specifica i dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. Per altre informazioni, vedere [matrici e Sized-Pointer attributi](array-and-sized-pointer-attributes.md), [**matrici**](arrays-1.md)e [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers). Il dichiaratore di parametro nel dichiaratore di funzione, ad esempio il nome del parametro, è facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nell'attributo **\[ in \]** è presente un attributo CONVERSE, **\[** [**out**](out-idl.md) **\]** , che indica che un parametro deve essere restituito dalla routine chiamata alla procedura chiamante. Gli attributi **\[ in \]** e **\[ out \]** sono noti come attributi di parametro direzionali perché specificano la direzione in cui vengono passati i parametri. Un parametro può essere definito come **\[ in \]**, **\[ out \]** o **\[ in**, **out \]**.

L'attributo **\[ in \]** identifica i parametri sottoposti a marshalling dallo stub client per la trasmissione al server.

Per impostazione predefinita, l'attributo **\[ in \]** viene applicato a un parametro quando non è specificato alcun attributo di parametro direzionale.

## <a name="examples"></a>Esempi

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_alloca utente \_ MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 