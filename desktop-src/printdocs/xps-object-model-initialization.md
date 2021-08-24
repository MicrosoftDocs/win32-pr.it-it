---
description: Viene descritto come inizializzare un OM XPS, che consente a un programma di creare un documento XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Inizializzare un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16edb992efee7c9cba1d5bc454ca5bcb44bd3267a2e91d4ca714120182df0657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946993"
---
# <a name="initialize-an-xps-om"></a>Inizializzare un OM XPS

Viene descritto come inizializzare un OM XPS, che consente a un programma di creare un documento XPS.

Le interfacce dell'API documento XPS vengono create da [**un'interfaccia IXpsOMObjectFactory.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) Per ottenere un puntatore a **un oggetto IXpsOMObjectFactory** che può essere usato nel programma, chiamare [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).

## <a name="code-example"></a>Esempio di codice

Nell'esempio seguente viene creata l'object factory che verrà usata per creare interfacce OM XPS in altri esempi.


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a>Procedure consigliate

È possibile rendere il programma più efficiente ottenendo un puntatore a un'interfaccia [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la prima volta che è necessario chiamare **IXpsOMObjectFactory** per creare un'interfaccia e quindi salvare il puntatore per l'uso in altre aree del programma. Quando l'object factory non è più necessaria o non è più necessaria per un periodo di tempo, il puntatore può essere rilasciato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Creare un OM XPS vuoto](create-a-blank-xps-om.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Per altre informazioni**
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
