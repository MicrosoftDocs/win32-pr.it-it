---
title: attributo helpstring
description: L'attributo \ helpstring \ specifica una stringa di caratteri utilizzata per descrivere l'elemento a cui si applica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- attributo MIDL di helpstring
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956386"
---
# <a name="helpstring-attribute"></a>attributo helpstring

L'attributo **\[ helpstring \]** specifica una stringa di caratteri utilizzata per descrivere l'elemento a cui si applica. È possibile applicare l'attributo **\[ helpstring \]** alle istruzioni Library, importlib, Interface, dispatch, Module o coclass, i typedef, le proprietà e i metodi.

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

*Guida-testo-stringa* 
</dt> <dd>

Stringa di caratteri con terminazione zero contenente il testo della guida.

</dd> <dt>

*facoltativo-Attribute-List* 
</dt> <dd>

Zero o più istruzioni di attributo MIDL.

</dd> <dt>

*elemento* 
</dt> <dd>

Una delle direttive seguenti: [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**coclass**](coclass.md).

</dd> <dt>

*Nome elemento* 
</dt> <dd>

Nome che altri componenti software possono usare per delineare l'elemento corrente

</dd> <dt>

*definizione* 
</dt> <dd>

Specifica le istruzioni che compongono la definizione dell'elemento.

</dd> <dt>

*IDL-Statement* 
</dt> <dd>

Un'istruzione di definizione dell'interfaccia MIDL, ad esempio [**propget**](propget.md) o [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare le funzioni [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nelle interfacce [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) per recuperare la stringa della guida.

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

[**libreria**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 