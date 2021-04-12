---
description: Viene descritto come inizializzare un oggetto XPS OM, che consente a un programma di creare un documento XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Inizializzare un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344831"
---
# <a name="initialize-an-xps-om"></a>Inizializzare un OM XPS

Viene descritto come inizializzare un oggetto XPS OM, che consente a un programma di creare un documento XPS.

Le interfacce dell'API documento XPS vengono create da un'interfaccia [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) . Per ottenere un puntatore a un **IXpsOMObjectFactory** che può essere usato nel programma, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Esempio di codice

Nell'esempio seguente viene creata la factory di oggetti che verrà utilizzata per creare interfacce XPS OM in altri esempi.


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

È possibile rendere più efficiente il programma ottenendo un puntatore a un'interfaccia [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la prima volta che è necessario chiamare **IXpsOMObjectFactory** per creare un'interfaccia e quindi salvare il puntatore per l'utilizzo in altre aree del programma. Quando il programma non necessita più dell'object factory o non lo richiede per un certo periodo di tempo, il puntatore può essere rilasciato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Creazione di un OM XPS vuoto](create-a-blank-xps-om.md)
</dt> <dt>

**Usato in questa sezione**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
