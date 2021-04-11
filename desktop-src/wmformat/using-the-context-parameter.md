---
title: Uso del parametro di contesto
description: Uso del parametro di contesto
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK, parametro di contesto
- Windows Media Format SDK, parametro pvContext
- parametro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117351"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="bf114-106">Uso del parametro di contesto</span><span class="sxs-lookup"><span data-stu-id="bf114-106">Using the Context Parameter</span></span>

<span data-ttu-id="bf114-107">Alcuni callback usati da Windows Media Format SDK accettano un parametro denominato *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="bf114-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="bf114-108">Gli oggetti chiamante passano lungo il valore specificato nel metodo che ha avviato l'azione asincrona.</span><span class="sxs-lookup"><span data-stu-id="bf114-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="bf114-109">Ad esempio, quando si chiama [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), è possibile passare un valore per *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="bf114-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="bf114-110">Quando il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) viene chiamato dall'oggetto Reader per notificare all'applicazione che il file è stato aperto, passerà qualsiasi valore usato nella chiamata per **aprirlo** come parametro *pvContext* di **OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="bf114-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="bf114-111">Questo parametro di contesto viene fornito per l'uso e può essere usato nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="bf114-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="bf114-112">Il parametro *pvContext* viene usato più spesso quando più oggetti devono condividere lo stesso callback.</span><span class="sxs-lookup"><span data-stu-id="bf114-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="bf114-113">Ad esempio, diversi oggetti usano il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="bf114-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="bf114-114">È possibile usare *pvContext* per consentire ai diversi oggetti di condividere un'implementazione di **OnStatus** passando un valore diverso per *pvContext* nella chiamata originale.</span><span class="sxs-lookup"><span data-stu-id="bf114-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="bf114-115">Nell'implementazione di **OnStatus** è possibile creare un ramo della logica di gestione dei messaggi in base al valore di *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="bf114-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf114-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf114-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf114-117">**Utilizzo dei metodi di callback**</span><span class="sxs-lookup"><span data-stu-id="bf114-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




