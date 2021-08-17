---
title: source (attributo)
description: L'attributo \ source\ indica che un membro di una coclasse, una proprietà o un metodo è un'origine di eventi. Per un membro di una coclasse, questo attributo indica che il membro viene chiamato anziché implementato.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- attributo di origine MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f7039505846d7a35bbd0e077456905c0d29ad13be398fe673ca5c1f8da25e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066681"
---
# <a name="source-attribute"></a>source (attributo)

**\[ \] L'attributo** di origine indica che un membro di [**una coclasse,**](coclass.md)una proprietà o un metodo è un'origine di eventi. Per un membro di una **coclasse**, questo attributo indica che il membro viene chiamato anziché implementato.

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*attributi di coclasse* 
</dt> <dd>

Zero o più attributi che verranno applicati alla [**coclasse**](coclass.md).

</dd> <dt>

*coclass-name* 
</dt> <dd>

Identificatore del nome della [**coclasse**](coclass.md).

</dd> <dt>

*attributi facoltativi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di istruzione* 
</dt> <dd>

Può essere [**un'interfaccia**](interface.md) [**o un'interfaccia dispatch.**](dispinterface.md)

</dd> <dt>

*statement-name* 
</dt> <dd>

Nome [**dell'interfaccia o**](interface.md) [**dell'interfaccia dispatch.**](dispinterface.md)

</dd> <dt>

*object-type* 
</dt> <dd>

Tipo dell'oggetto restituito dal metodo. Questo oggetto è un'origine di eventi.

</dd> <dt>

*function-name* 
</dt> <dd>

Nome di un metodo in [**un'interfaccia o**](interface.md) [**interfaccia dispatch.**](dispinterface.md)

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Zero o più parametri di metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una proprietà o in un metodo, **\[ \] l'attributo** di origine indica che il membro restituisce un oggetto o VARIANT che è un'origine di eventi. L'oggetto implementa **IConnectionPointContainer.**

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ SOURCE, FUNCFLAG \_ SOURCE

## <a name="examples"></a>Esempi

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 