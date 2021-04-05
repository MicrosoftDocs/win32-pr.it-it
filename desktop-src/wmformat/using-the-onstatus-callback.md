---
title: Uso del callback di OnStatus
description: Uso del callback di OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK, metodo OnStatus callback
- Windows Media Format SDK, interfaccia IWMStatusCallback
- Metodo di callback OnStatus, informazioni
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956168"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="b1dfb-107">Uso del callback di OnStatus</span><span class="sxs-lookup"><span data-stu-id="b1dfb-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="b1dfb-108">Il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback viene chiamato da diversi oggetti in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="b1dfb-109">**OnStatus** riceve messaggi che rappresentano le modifiche dello stato delle operazioni SDK.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="b1dfb-110">Per usare il metodo di callback **OnStatus** , è necessario implementare una classe nell'applicazione che eredita dall'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) .</span><span class="sxs-lookup"><span data-stu-id="b1dfb-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="b1dfb-111">Includere il codice per la versione di **OnStatus** nella classe.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="b1dfb-112">Alcuni esempi di implementazioni di **OnStatus** sono disponibili negli esempi inclusi in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="b1dfb-113">Per ulteriori informazioni sugli esempi, vedere [applicazioni di esempio](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b1dfb-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="b1dfb-114">È necessario associare l'implementazione del callback di stato a vari oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="b1dfb-115">Ogni oggetto ha un modo diverso per effettuare questa associazione.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="b1dfb-116">Per un elenco dei metodi che associano oggetti specifici, vedere la pagina di riferimento di **IWMStatusCallback** .</span><span class="sxs-lookup"><span data-stu-id="b1dfb-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="b1dfb-117">I messaggi di stato che possono essere ricevuti da **OnStatus** sono definiti nel tipo di enumerazione [**\_ dello stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="b1dfb-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="b1dfb-118">È possibile scegliere i messaggi da intercettare e quali ignorare.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="b1dfb-119">Tuttavia, per determinate funzionalità è necessaria la risposta ad alcuni messaggi di stato.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="b1dfb-120">Ad esempio, quando si usa il Reader asincrono, il metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) apre un file in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="b1dfb-121">L'unico modo per stabilire quando il file è stato aperto consiste nel intercettare il \_ messaggio aperto MWT.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="b1dfb-122">In genere, i messaggi a cui si risponde sono notifiche del completamento delle attività asincrone.</span><span class="sxs-lookup"><span data-stu-id="b1dfb-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1dfb-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1dfb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1dfb-124">**Utilizzo dei metodi di callback**</span><span class="sxs-lookup"><span data-stu-id="b1dfb-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




