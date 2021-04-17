---
title: struct (attributo)
description: La parola chiave struct viene usata in un identificatore del tipo di struttura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- attributo struct MIDL
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299736"
---
# <a name="struct-attribute"></a>struct (attributo)

La parola chiave **struct** viene usata in un identificatore del tipo di struttura.

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*struct-Tag* 
</dt> <dd>

Specifica un tag facoltativo per la struttura.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano al membro della struttura. Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** e **\[** [**size \_ è**](size-is.md) **\]** ; la stringa degli attributi **\[** [](string.md) **\]** di utilizzo e **\[** [**Ignore**](ignore.md), **\]** l'attributo Pointer **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** e il **\[** [**\_ tipo di opzione**](switch-type.md)attribute Union **\]** . Separare più attributi di campo con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno **struct**, un' [**Unione**](union.md)o un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote. Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'identificatore del tipo di struttura IDL, **struct**, differisce dall'identificatore di tipo C standard nei modi seguenti:

-   Ogni membro della struttura può essere associato a attributi di campo facoltativi che descrivono le caratteristiche del membro della struttura ai fini di una chiamata di procedura remota.
-   I campi di bit e i dichiaratori di funzione non sono consentiti nelle strutture utilizzate nelle chiamate a procedure remote. Questi costrutti di dichiaratori C standard possono essere usati solo se la struttura non è trasmessa sulla rete.

La forma delle strutture deve essere la stessa nelle diverse piattaforme per garantire l'interconnettività.

## <a name="examples"></a>Esempi

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**/c \_ ext**](-c-ext.md)
</dt> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**il primo \_ è**](first-is.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorare**](ignore.md)
</dt> <dt>

[**ultimo \_ è**](last-is.md)
</dt> <dt>

[**lunghezza \_**](length-is.md)
</dt> <dt>

[**Max \_ è**](max-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**dimensioni \_**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> <dt>

[**Unione**](union.md)
</dt> <dt>

[**unico**](unique.md)
</dt> </dl>

 

 