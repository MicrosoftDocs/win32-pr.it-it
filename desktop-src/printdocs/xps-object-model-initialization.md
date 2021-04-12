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
# <a name="initialize-an-xps-om"></a><span data-ttu-id="b758b-103">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="b758b-103">Initialize an XPS OM</span></span>

<span data-ttu-id="b758b-104">Viene descritto come inizializzare un oggetto XPS OM, che consente a un programma di creare un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b758b-104">Describes how to initialize an XPS OM, which allows a program to create an XPS document.</span></span>

<span data-ttu-id="b758b-105">Le interfacce dell'API documento XPS vengono create da un'interfaccia [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) .</span><span class="sxs-lookup"><span data-stu-id="b758b-105">The interfaces of the XPS Document API are created by an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface.</span></span> <span data-ttu-id="b758b-106">Per ottenere un puntatore a un **IXpsOMObjectFactory** che può essere usato nel programma, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="b758b-106">To obtain a pointer to an **IXpsOMObjectFactory** that can be used in your program, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="b758b-107">Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-107">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="b758b-108">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="b758b-108">Code Example</span></span>

<span data-ttu-id="b758b-109">Nell'esempio seguente viene creata la factory di oggetti che verrà utilizzata per creare interfacce XPS OM in altri esempi.</span><span class="sxs-lookup"><span data-stu-id="b758b-109">The following example creates the object factory that will be used to create XPS OM interfaces in other examples.</span></span>


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



## <a name="best-practices"></a><span data-ttu-id="b758b-110">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="b758b-110">Best Practices</span></span>

<span data-ttu-id="b758b-111">È possibile rendere più efficiente il programma ottenendo un puntatore a un'interfaccia [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) la prima volta che è necessario chiamare **IXpsOMObjectFactory** per creare un'interfaccia e quindi salvare il puntatore per l'utilizzo in altre aree del programma.</span><span class="sxs-lookup"><span data-stu-id="b758b-111">You can make your program more efficient by obtaining a pointer to an [**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) interface the first time that you need to call **IXpsOMObjectFactory** to create an interface, and then saving the pointer for use in other areas of the program.</span></span> <span data-ttu-id="b758b-112">Quando il programma non necessita più dell'object factory o non lo richiede per un certo periodo di tempo, il puntatore può essere rilasciato.</span><span class="sxs-lookup"><span data-stu-id="b758b-112">When the program no longer needs the object factory, or will not need it for a while, the pointer can be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b758b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b758b-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b758b-114">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="b758b-114">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="b758b-115">Creazione di un OM XPS vuoto</span><span class="sxs-lookup"><span data-stu-id="b758b-115">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

<span data-ttu-id="b758b-116">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="b758b-116">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="b758b-117">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="b758b-117">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="b758b-118">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b758b-118">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

<span data-ttu-id="b758b-119">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="b758b-119">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="b758b-120">Packaging</span><span class="sxs-lookup"><span data-stu-id="b758b-120">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="b758b-121">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="b758b-121">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="b758b-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b758b-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
