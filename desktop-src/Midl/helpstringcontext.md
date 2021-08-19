---
title: Attributo helpstringcontext
description: L'attributo \ helpstringcontext\ specifica un identificatore di contesto della Guida a 32 bit nel file della Guida. È possibile applicare l'attributo \ helpstringcontext\ a libreria, interfaccia, interfaccia dispatch, modulo, coclasse, istruzioni typedef, proprietà, parametri e metodi.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- Attributo helpstringcontext MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64e97ea0d7b41d87ef1d535d562f3b515dda4f59a67f6d5e35f97bed8b1f9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807236"
---
# <a name="helpstringcontext-attribute"></a>Attributo helpstringcontext

**\[ L'attributo \] helpstringcontext** specifica un identificatore di contesto della Guida a 32 bit nel file della Guida. È possibile applicare l'attributo **\[ helpstringcontext \]** alla [**libreria,**](library.md)all'interfaccia [**,**](interface.md) [**all'interfaccia**](dispinterface.md) [**,**](module.md)al modulo, alla [**coclasse,**](coclass.md)alle [**istruzioni typedef,**](typedef.md) alle proprietà, ai parametri e ai metodi.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*contextid* 
</dt> <dd>

Intero univoco che identifica il testo della Guida associato all'istruzione MIDL corrente.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*idl-statement* 
</dt> <dd>

Istruzione MIDL a cui verrà applicato **\[ l'attributo helpstringcontext. \]**

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare le **funzioni GetDocumentation2** nelle **interfacce ITypeLib2** e **ITypeInfo2** per recuperare la stringa della Guida.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




