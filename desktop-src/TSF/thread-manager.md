---
title: Gestione thread
description: Gestione thread è il componente di base del gestore di TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Framework servizi di testo (TSF), gestione thread
- TSF (Text Services Framework), gestione thread
- Servizi di testo, gestione thread
- Applicazioni abilitate per TSF, gestione thread
- gestione thread
- Gestione TSF
- notifiche di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046991"
---
# <a name="thread-manager"></a><span data-ttu-id="4f385-110">Gestione thread</span><span class="sxs-lookup"><span data-stu-id="4f385-110">Thread Manager</span></span>

<span data-ttu-id="4f385-111">Gestione thread è il componente di base del gestore di TSF.</span><span class="sxs-lookup"><span data-stu-id="4f385-111">The thread manager is the base component of the TSF manager.</span></span> <span data-ttu-id="4f385-112">Gestione thread esegue attività comuni correlate alle applicazioni e ai servizi di testo (client).</span><span class="sxs-lookup"><span data-stu-id="4f385-112">The thread manager performs common tasks related to both applications and text services (clients).</span></span> <span data-ttu-id="4f385-113">Queste attività includono, ad esempio, l'attivazione e la disattivazione di servizi di testo TSF, la creazione di gestori di documenti e la manutenzione della relazione corretta tra documenti e lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="4f385-113">These tasks include, but are not limited to, the activation and deactivation of TSF text services, the creation of document managers, and maintenance of the proper relationship between documents and the input focus.</span></span> <span data-ttu-id="4f385-114">Gestione thread viene definito dall'interfaccia [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .</span><span class="sxs-lookup"><span data-stu-id="4f385-114">The thread manager is defined by the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface.</span></span>

<span data-ttu-id="4f385-115">La maggior parte delle interfacce e degli oggetti forniti dal gestore di TSF può essere ottenuta usando i metodi forniti dall'interfaccia del gestore di thread.</span><span class="sxs-lookup"><span data-stu-id="4f385-115">The majority of the interfaces and objects provided by the TSF manager can be obtained using the methods that the thread manager interface provides.</span></span>

## <a name="applications"></a><span data-ttu-id="4f385-116">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="4f385-116">Applications</span></span>

<span data-ttu-id="4f385-117">Un'applicazione crea un oggetto gestore thread chiamando [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ TFThreadMgr.</span><span class="sxs-lookup"><span data-stu-id="4f385-117">An application creates a thread manager object by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_TFThreadMgr.</span></span>

## <a name="text-services"></a><span data-ttu-id="4f385-118">Servizi di testo</span><span class="sxs-lookup"><span data-stu-id="4f385-118">Text Services</span></span>

<span data-ttu-id="4f385-119">Un servizio di testo ottiene un oggetto gestore thread nel metodo [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) del servizio di testo.</span><span class="sxs-lookup"><span data-stu-id="4f385-119">A text service obtains a thread manager object in the text service [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span>

## <a name="event-notifications"></a><span data-ttu-id="4f385-120">Notifiche degli eventi</span><span class="sxs-lookup"><span data-stu-id="4f385-120">Event Notifications</span></span>

<span data-ttu-id="4f385-121">Gestione thread fornisce inoltre la notifica degli eventi ai client.</span><span class="sxs-lookup"><span data-stu-id="4f385-121">The thread manager also provides event notification to clients.</span></span> <span data-ttu-id="4f385-122">In TSF, le notifiche degli eventi vengono fornite per mezzo di un sink di evento, ovvero un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="4f385-122">In TSF, event notifications are provided by means of an event sink, which is a COM object.</span></span> <span data-ttu-id="4f385-123">Per ricevere notifiche da gestione thread, un client implementa un oggetto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e installa il sink di evento.</span><span class="sxs-lookup"><span data-stu-id="4f385-123">To receive notifications from the thread manager, a client implements an [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) object and installs the event sink.</span></span> <span data-ttu-id="4f385-124">Il sink di evento viene installato eseguendo una query su gestione thread per IID \_ ITfSource e chiamando [ITfSource:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfThreadMgrEventSink.</span><span class="sxs-lookup"><span data-stu-id="4f385-124">The event sink is installed by querying the thread manager for IID\_ITfSource and calling [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfThreadMgrEventSink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f385-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f385-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f385-126">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="4f385-126">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="4f385-127">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4f385-127">CoCreateInstance</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="4f385-128">ITfTextInputProcessor:: Activate</span><span class="sxs-lookup"><span data-stu-id="4f385-128">ITfTextInputProcessor::Activate</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="4f385-129">ITfThreadMgrEventSink</span><span class="sxs-lookup"><span data-stu-id="4f385-129">ITfThreadMgrEventSink</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[<span data-ttu-id="4f385-130">ITfSource:: AdviseSink</span><span class="sxs-lookup"><span data-stu-id="4f385-130">ITfSource::AdviseSink</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 