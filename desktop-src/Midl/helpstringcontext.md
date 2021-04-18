---
title: attributo helpstringcontext
description: L'attributo \ helpstringcontext \ specifica un identificatore di contesto della guida a 32 bit nel file della guida. È possibile applicare l'attributo \ helpstringcontext \ a librerie, interfacce, interfacce dispatch, moduli, coclassi, istruzioni typedef, proprietà, parametri e metodi.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- attributo MIDL di helpstringcontext
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299083"
---
# <a name="helpstringcontext-attribute"></a>attributo helpstringcontext

L'attributo **\[ helpstringcontext \]** specifica un identificatore di contesto della guida a 32 bit nel file della guida. È possibile applicare l' **\[ attributo \] helpstringcontext** a [**librerie**](library.md), [**interfacce, interfacce**](interface.md) [**Dispatch**](dispinterface.md), [**moduli**](module.md), [**coclassi**](coclass.md), istruzioni [**typedef**](typedef.md) , proprietà, parametri e metodi.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ContextId* 
</dt> <dd>

Intero univoco che identifica il testo della Guida associato all'istruzione MIDL corrente.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Zero o più attributi MIDL.

</dd> <dt>

*IDL-Statement* 
</dt> <dd>

Istruzione MIDL a cui verrà applicato l'attributo **\[ helpstringcontext \]** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare le funzioni **GetDocumentation2** nelle interfacce **ITypeLib2** e **ITypeInfo2** per recuperare la stringa della guida.

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

 

 




