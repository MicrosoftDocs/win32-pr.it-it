---
title: ms_union (attributo)
description: La parola chiave \ms \_ union\ viene usata per controllare l'allineamento del rapporto di mancato recapito delle unioni non incapsulate.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union attributo MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 860054fe26657c4028c172da08e0c56dbf6ae257ffc98e79905f8420b54e6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642799"
---
# <a name="ms_union-attribute"></a>Attributo ms \_ union

La parola \[ **chiave ms \_ union** \] viene usata per controllare l'allineamento NDR delle unioni non incapsulate.

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*procedure-type* 
</dt> <dd>

Specifica il tipo restituito della routine a cui viene applicato l'attributo.

</dd> <dt>

*procedure-name* 
</dt> <dd>

Specifica il nome della routine.

</dd> <dt>

*param-list* 
</dt> <dd>

Specifica l'elenco di parametri della procedura, che può essere vuoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non usare mai questa opzione o attributo con nuove interfacce. Si tratta solo di una funzionalità di compatibilità con le versioni precedenti. Il compilatore MIDL in questa versione di Microsoft RPC rispecchia il comportamento del compilatore IDL DCE OSF per le unioni non incapsulate. Tuttavia, poiché le versioni precedenti del compilatore MIDL non lo hanno fatto, l'opzione [**/ms \_ union**](-ms-union.md) garantisce la compatibilità con le interfacce compilate nelle versioni precedenti del compilatore MIDL.

La **funzionalità ms \_ union** può essere usata come attributo di interfaccia IDL, attributo di tipo IDL o come opzione della riga di comando ( [**/ms \_ union**](-ms-union.md)).

## <a name="examples"></a>Esempi

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/ms \_ union**](-ms-union.md)
</dt> </dl>

 

 




