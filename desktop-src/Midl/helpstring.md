---
title: Attributo helpstring
description: L'attributo \ helpstring\ specifica una stringa di caratteri usata per descrivere l'elemento a cui si applica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- Attributo helpstring MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abb433d7112bc4c3257345d086ccf308cc1892b61a99991b485ce4962b5851e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013869"
---
# <a name="helpstring-attribute"></a>Attributo helpstring

**\[ L'attributo \] helpstring** specifica una stringa di caratteri usata per descrivere l'elemento a cui si applica. È possibile applicare l'attributo **\[ helpstring \]** a istruzioni library, importlib, interface, dispinterface, module o coclass, typedef, proprietà e metodi.

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*help-text-string* 
</dt> <dd>

Stringa di caratteri con terminazione zero contenente il testo della Guida.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Zero o più istruzioni di attributo MIDL.

</dd> <dt>

*Elemento* 
</dt> <dd>

Una delle direttive seguenti: [**library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property** o [**coclass**](coclass.md).

</dd> <dt>

*element-name* 
</dt> <dd>

Nome che altri componenti software possono usare per delineare l'elemento corrente

</dd> <dt>

*Definizione* 
</dt> <dd>

Specifica le istruzioni che costituiscono la definizione dell'elemento.

</dd> <dt>

*idl-statement* 
</dt> <dd>

Istruzione di definizione dell'interfaccia MIDL, ad [**esempio propget**](propget.md) o [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare le [**funzioni GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nelle [**interfacce ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) per recuperare la stringa della Guida.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Libreria**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**Modulo**](module.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 