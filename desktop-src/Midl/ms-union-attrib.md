---
title: ms_union (attributo)
description: La parola chiave \ MS \_ Union \ viene utilizzata per controllare l'allineamento del rapporto di recapito delle unioni non incapsulate.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- attributo ms_union MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045568"
---
# <a name="ms_union-attribute"></a>\_attributo ms Union

La parola chiave \[ **MS \_ Union** \] viene utilizzata per controllare l'allineamento del rapporto di recapito delle unioni non incapsulate.

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

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*tipo di procedura* 
</dt> <dd>

Specifica il tipo restituito della routine a cui viene applicato l'attributo.

</dd> <dt>

*nome procedura* 
</dt> <dd>

Specifica il nome della stored procedure.

</dd> <dt>

*param-list* 
</dt> <dd>

Specifica l'elenco di parametri della stored procedure, che può essere vuoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non usare mai questa opzione o attributo con nuove interfacce. Si tratta di una funzionalità di compatibilità con le versioni precedenti. Il compilatore MIDL in questa versione di Microsoft RPC rispecchia il comportamento del compilatore IDL OSF DCE per le unioni non incapsulate. Tuttavia, poiché le versioni precedenti del compilatore MIDL non lo hanno fatto, l' [**opzione \_ Union/MS**](-ms-union.md) fornisce la compatibilità con le interfacce compilate in versioni precedenti del compilatore MIDL.

La funzionalità di **MS \_ Union** può essere utilizzata come attributo di interfaccia IDL, attributo di tipo IDL o come opzione della riga di comando ( [**/MS \_ Union**](-ms-union.md)).

## <a name="examples"></a>Esempi

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_Unione/MS**](-ms-union.md)
</dt> </dl>

 

 




