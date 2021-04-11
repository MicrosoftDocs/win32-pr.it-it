---
title: Informazioni sui controlli Rich Edit senza finestra
description: Un controllo Rich Edit senza finestra, noto anche come oggetto servizi di testo, è un oggetto che fornisce la funzionalità di un controllo Rich Edit senza fornire la finestra.
ms.assetid: 880a704d-776a-49d3-be31-0328af408e3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1c8bc685dff5f8ddb041011089a84eb2e12008
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963477"
---
# <a name="about-windowless-rich-edit-controls"></a><span data-ttu-id="b502e-103">Informazioni sui controlli Rich Edit senza finestra</span><span class="sxs-lookup"><span data-stu-id="b502e-103">About Windowless Rich Edit Controls</span></span>

<span data-ttu-id="b502e-104">Un controllo Rich Edit senza finestra, noto anche come oggetto servizi di testo, è un oggetto che fornisce la funzionalità di un [controllo Rich Edit](rich-edit-controls.md) senza fornire la finestra.</span><span class="sxs-lookup"><span data-stu-id="b502e-104">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span> <span data-ttu-id="b502e-105">Per fornire la funzionalità di una finestra, ad esempio la possibilità di ricevere messaggi e un contesto di dispositivo in cui è possibile creare, i controlli Rich Edit senza finestra usano una coppia di interfacce: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="b502e-105">To provide the functionality of a window, such as the ability to receive messages and a device context into which it can draw, windowless rich edit controls use a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

<span data-ttu-id="b502e-106">Per creare un controllo Rich Edit senza finestra, chiamare la funzione [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) con un puntatore all'implementazione dell'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="b502e-106">To create a windowless rich edit control, call the [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function with a pointer to your implementation of the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span> <span data-ttu-id="b502e-107">**CreateTextServices** restituisce un puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) su cui è possibile eseguire una query per recuperare un puntatore all'implementazione [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) del controllo privo di finestra.</span><span class="sxs-lookup"><span data-stu-id="b502e-107">**CreateTextServices** returns an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer that you can query to retrieve a pointer to the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) implementation of the windowless control.</span></span>

<span data-ttu-id="b502e-108">Msftedit.dll esporta un identificatore di interfaccia (IID) denominato **IID \_ ITextServices** che è possibile usare per eseguire una query sul puntatore [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per l'interfaccia [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="b502e-108">Msftedit.dll exports an interface identifier (IID) called **IID\_ITextServices** that you can use to query the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer for the [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="b502e-109">Nell'esempio seguente viene illustrato come recuperare **IID \_ ITextServices** e usarlo per ottenere l'interfaccia **ITextServices** .</span><span class="sxs-lookup"><span data-stu-id="b502e-109">The following example shows how to retrieve **IID\_ITextServices** and use it to get the **ITextServices** interface.</span></span>


```
    .
    .
    .
    HRESULT hr;
    IUnknown* pUnk = NULL;
    ITextServices* pTextServices =  NULL;
    
    // Create an instance of the application-defined object that implements the 
    // ITextHost interface.
    TextHost* pTextHost = new TextHost();
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from 
    // Msftedit.dll. The hmodRichEdit parameter is a handle to the 
    // Msftedit.dll module retrieved by a previous call to the 
    // GetModuleHandle function.
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, 
        "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    if (FAILED(hr))
        goto errorHandler;
     .
     . 
     .   
     
```



<span data-ttu-id="b502e-110">Msftedit.dll esporta anche un identificatore di interfaccia (IID) denominato **IID \_ ITextHost** che può essere usato in modo analogo per eseguire query per l'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) .</span><span class="sxs-lookup"><span data-stu-id="b502e-110">Msftedit.dll also exports an interface identifier (IID) called **IID\_ITextHost** that can be used in a similar manner to query for the [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface.</span></span>

<span data-ttu-id="b502e-111">L'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) dispone di metodi che il controllo senza finestra chiama per recuperare informazioni sulla finestra.</span><span class="sxs-lookup"><span data-stu-id="b502e-111">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface has methods that the windowless control calls to retrieve information about your window.</span></span> <span data-ttu-id="b502e-112">Ad esempio, l'oggetto servizi di testo chiama il metodo [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) per recuperare un contesto di dispositivo in cui può essere disegnato.</span><span class="sxs-lookup"><span data-stu-id="b502e-112">For example, the text services object calls the [**TxGetDC**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetdc) method to retrieve a device context into which it can draw.</span></span> <span data-ttu-id="b502e-113">Il controllo senza finestra chiama il metodo [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) per l'invio di notifiche, ad esempio i messaggi di notifica Rich Edit, all'host di testo.</span><span class="sxs-lookup"><span data-stu-id="b502e-113">The windowless control calls the [**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method to send notifications, such as the rich edit notification messages, to the text host.</span></span> <span data-ttu-id="b502e-114">L'oggetto servizi di testo chiama altri metodi **ITextHost** per richiedere all'host di testo di eseguire altri servizi correlati alla finestra.</span><span class="sxs-lookup"><span data-stu-id="b502e-114">The text services object calls other **ITextHost** methods to request the text host to perform other window-related services.</span></span> <span data-ttu-id="b502e-115">Ad esempio, il metodo [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) richiede all'host di testo di aggiungere un rettangolo all'area di aggiornamento della finestra.</span><span class="sxs-lookup"><span data-stu-id="b502e-115">For example, the [**TxInvalidateRect**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txinvalidaterect) method requests the text host to add a rectangle to the window's update region.</span></span>

<span data-ttu-id="b502e-116">Un controllo Rich Edit standard prevede una procedura finestra che elabora messaggi di sistema e messaggi dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b502e-116">A standard rich edit control has a window procedure that processes system messages and messages from your application.</span></span> <span data-ttu-id="b502e-117">È possibile usare l'handle della finestra del controllo per inviare i messaggi per l'esecuzione di modifiche del testo e altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="b502e-117">You can use the control's window handle to send it messages for performing text editing and other operations.</span></span> <span data-ttu-id="b502e-118">Tuttavia, un controllo Rich Edit senza finestra non ha alcuna routine di finestra per la ricezione e l'elaborazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="b502e-118">But a windowless rich edit control has no window procedure to receive and process messages.</span></span> <span data-ttu-id="b502e-119">Fornisce invece un'interfaccia [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .</span><span class="sxs-lookup"><span data-stu-id="b502e-119">Instead, it provides an [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) interface.</span></span> <span data-ttu-id="b502e-120">Per inviare messaggi a un controllo Rich Edit senza finestra, chiamare il metodo [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) .</span><span class="sxs-lookup"><span data-stu-id="b502e-120">To send messages to a windowless rich edit control, call the [**TxSendMessage**](/windows/desktop/api/Textserv/nf-textserv-itextservices-txsendmessage) method.</span></span> <span data-ttu-id="b502e-121">È possibile utilizzare questo metodo per inviare qualsiasi messaggio Rich Edit o per passare altri messaggi che interessano il controllo, ad esempio i messaggi di sistema per l'input del mouse o della tastiera.</span><span class="sxs-lookup"><span data-stu-id="b502e-121">You can use this method to send any of the rich edit messages or to pass on other messages that affect the control, such as system messages for mouse or keyboard input.</span></span>

<span data-ttu-id="b502e-122">È anche possibile creare l'oggetto servizi di testo come parte di un [oggetto aggregato com](/windows/desktop/com/aggregation).</span><span class="sxs-lookup"><span data-stu-id="b502e-122">You can also create the text services object as part of a [COM-aggregated object](/windows/desktop/com/aggregation).</span></span> <span data-ttu-id="b502e-123">In questo modo è più semplice aggregare l'oggetto servizi di testo con un oggetto Component Object Model senza finestra (COM).</span><span class="sxs-lookup"><span data-stu-id="b502e-123">This makes it easy to aggregate the text services object with a windowless Component Object Model (COM) object.</span></span>

 

 