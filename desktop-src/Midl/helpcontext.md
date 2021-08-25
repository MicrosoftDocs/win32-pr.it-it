---
title: helpcontext (attributo)
description: L'attributo \ helpcontext\ specifica un identificatore di contesto che consente all'utente di visualizzare le informazioni su questo elemento nel file della Guida.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- Attributo helpcontext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3caa5dd32257fb5d75bbf77cde4ae5e71c6e97574cd1c263ead47aacedccadc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895251"
---
# <a name="helpcontext-attribute"></a>helpcontext (attributo)

\[ **L'attributo helpcontext** specifica un identificatore di contesto che consente all'utente di visualizzare le informazioni su \] questo elemento nel file della Guida.

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*uuid-number* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**libreria**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[ property \]** o [**coclass**](coclass.md).

</dd> <dt>

*helpcontext-value* 
</dt> <dd>

Intero univoco che identifica il testo della Guida associato all'elemento MIDL corrente.

</dd> <dt>

*attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi applicabili all'intero elemento MIDL.

</dd> <dt>

*Elemento* 
</dt> <dd>

Una delle direttive seguenti: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property** o [**coclass**](coclass.md).

</dd> <dt>

*element-name* 
</dt> <dd>

Nome che altri componenti software possono usare per delineare l'elemento corrente.

</dd> <dt>

*Definizioni* 
</dt> <dd>

Specifica le istruzioni che costituiscono la definizione dell'elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo helpcontext può essere applicato agli elementi \[  \] seguenti: [**library**](library.md), \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property** o [**coclass**](coclass.md).

*Helpcontext-value* è un identificatore di contesto a 32 bit all'interno del file della Guida che può essere recuperato con le funzioni [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nelle [**interfacce ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo.**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo)

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**Libreria**](library.md)
</dt> <dt>

[**Modulo**](module.md)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 