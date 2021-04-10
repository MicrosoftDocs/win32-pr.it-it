---
title: source (attributo)
description: L'attributo \ source \ indica che un membro di una coclasse, di una proprietà o di un metodo è un'origine di eventi. Per un membro di una coclasse, questo attributo indica che il membro viene chiamato anziché implementato.
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
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956372"
---
# <a name="source-attribute"></a>source (attributo)

L'attributo di **\[ origine \]** indica che un membro di una [**coclasse**](coclass.md), di una proprietà o di un metodo è un'origine di eventi. Per un membro di una **coclasse**, questo attributo indica che il membro viene chiamato anziché implementato.

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

*coclass-attributi* 
</dt> <dd>

Zero o più attributi che verranno applicati alla [**coclasse**](coclass.md).

</dd> <dt>

*coclass-nome* 
</dt> <dd>

Identificatore del nome della [**coclasse**](coclass.md).

</dd> <dt>

*facoltativo-attributi* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*tipo di istruzione* 
</dt> <dd>

Può essere [**Interface**](interface.md) o [**Dispatch**](dispinterface.md).

</dd> <dt>

*nome istruzione* 
</dt> <dd>

Nome dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).

</dd> <dt>

*tipo oggetto* 
</dt> <dd>

Tipo dell'oggetto restituito dal metodo. Questo oggetto è un'origine di eventi.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Nome di un metodo in un'interfaccia o in un' [**interfaccia**](interface.md) [**Dispatch**](dispinterface.md).

</dd> <dt>

*facoltativo-parameter-list* 
</dt> <dd>

Zero o più parametri del metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una proprietà o un metodo l'attributo di **\[ origine \]** indica che il membro restituisce un oggetto o una variante che è un'origine di eventi. L'oggetto implementa **IConnectionPointContainer**.

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ source, FUNCFLAG \_ source

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

[**interfaccia**](interface.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 