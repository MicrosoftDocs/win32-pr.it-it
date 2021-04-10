---
title: helpcontext (attributo)
description: L'attributo \ HelpContext \ specifica un identificatore di contesto che consente all'utente di visualizzare informazioni sull'elemento nel file della guida.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- attributo MIDL di HelpContext
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956399"
---
# <a name="helpcontext-attribute"></a>helpcontext (attributo)

L' \[ attributo **HelpContext** \] specifica un identificatore di contesto che consente all'utente di visualizzare informazioni sull'elemento nel file della guida.

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

*UUID-numero* 
</dt> <dd>

Specifica un numero di identificazione univoco universale per la [**libreria**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Methods**, **\[ Property \]** o [**coclass**](coclass.md).

</dd> <dt>

*HelpContext-valore* 
</dt> <dd>

Intero univoco che identifica il testo della Guida associato all'elemento MIDL corrente.

</dd> <dt>

*elenco attributi* 
</dt> <dd>

Specifica un elenco di uno o più attributi applicabili all'elemento MIDL nel suo complesso.

</dd> <dt>

*elemento* 
</dt> <dd>

Una delle direttive seguenti: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**coclass**](coclass.md).

</dd> <dt>

*Nome elemento* 
</dt> <dd>

Nome che altri componenti software possono utilizzare per delineare l'elemento corrente.

</dd> <dt>

*definizioni* 
</dt> <dd>

Specifica le istruzioni che compongono la definizione dell'elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

L' \[ **attributo HelpContext** \] può essere applicato agli elementi seguenti: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**coclass**](coclass.md).

*HelpContext-value* è un identificatore di contesto a 32 bit all'interno del file della guida che può essere recuperato con le funzioni [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nelle interfacce [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .

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

[**interfaccia**](interface.md)
</dt> <dt>

[**libreria**](library.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 