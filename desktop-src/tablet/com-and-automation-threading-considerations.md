---
description: Le seguenti considerazioni relative al threading di Tablet PC sono specifiche di quando vengono usati Component Object Model (COM) e l'automazione.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Considerazioni sul threading di automazione e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305694"
---
# <a name="com-and-automation-threading-considerations"></a><span data-ttu-id="df33c-103">Considerazioni sul threading di automazione e COM</span><span class="sxs-lookup"><span data-stu-id="df33c-103">COM and Automation Threading Considerations</span></span>

<span data-ttu-id="df33c-104">Le seguenti considerazioni relative al threading di Tablet PC sono specifiche di quando vengono usati Component Object Model (COM) e l'automazione.</span><span class="sxs-lookup"><span data-stu-id="df33c-104">The following Tablet PC threading considerations are specific to when Component Object Model (COM) and Automation are used.</span></span>

-   [<span data-ttu-id="df33c-105">Thread safety</span><span class="sxs-lookup"><span data-stu-id="df33c-105">Thread Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="df33c-106">Applicazioni STA e MTA</span><span class="sxs-lookup"><span data-stu-id="df33c-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="df33c-107">InkCollector e InkOverlay</span><span class="sxs-lookup"><span data-stu-id="df33c-107">InkCollector and InkOverlay</span></span>](#inkcollector-and-inkoverlay)
-   [<span data-ttu-id="df33c-108">Sink di evento</span><span class="sxs-lookup"><span data-stu-id="df33c-108">Event Sinks</span></span>](#event-sinks)
-   [<span data-ttu-id="df33c-109">Eccezioni nei gestori eventi</span><span class="sxs-lookup"><span data-stu-id="df33c-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="df33c-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df33c-110">Related topics</span></span>](#related-topics)

## <a name="thread-safety"></a><span data-ttu-id="df33c-111">Thread safety</span><span class="sxs-lookup"><span data-stu-id="df33c-111">Thread Safety</span></span>

<span data-ttu-id="df33c-112">Ad eccezione dei controlli [InkPicture](inkpicture-control.md) e [InkEdit](inkedit-control.md) , gli oggetti Tablet PC sono thread-safe e sono contrassegnati come entrambi.</span><span class="sxs-lookup"><span data-stu-id="df33c-112">Except for the [InkPicture](inkpicture-control.md) and [InkEdit](inkedit-control.md) controls, Tablet PC objects are thread-safe and are marked as both.</span></span> <span data-ttu-id="df33c-113">Essendo contrassegnate come entrambe, possono essere eseguite in un Apartment a thread singolo (STA) o in un Apartment a thread multipli (MTA).</span><span class="sxs-lookup"><span data-stu-id="df33c-113">By being marked as both, they can run in either a single threaded apartment (STA) or a multithreaded apartment (MTA).</span></span>

<span data-ttu-id="df33c-114">Windows Form usa il modello STA perché Windows Forms è basato su finestre Win32 native che sono intrinsecamente thread-apartment.</span><span class="sxs-lookup"><span data-stu-id="df33c-114">Windows forms use the STA model because windows forms are based on native Win32 windows that are inherently apartment threaded.</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="df33c-115">Applicazioni STA e MTA</span><span class="sxs-lookup"><span data-stu-id="df33c-115">STA and MTA Applications</span></span>

<span data-ttu-id="df33c-116">Se l'applicazione viene eseguita in un MTA o utilizza il gestore di marshalling a thread libero (FTM), è necessario scrivere codice thread-safe; Tuttavia, in questo modo è possibile migliorare determinati problemi di prestazioni di gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="df33c-116">If your application runs in an MTA or uses the free threaded marshaler (FTM), you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

## <a name="inkcollector-and-inkoverlay"></a><span data-ttu-id="df33c-117">InkCollector e InkOverlay</span><span class="sxs-lookup"><span data-stu-id="df33c-117">InkCollector and InkOverlay</span></span>

<span data-ttu-id="df33c-118">L'applicazione non deve rilasciare il riferimento finale all'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) , eliminando così l'oggetto direttamente dal thread di input penna.</span><span class="sxs-lookup"><span data-stu-id="df33c-118">Your application should not release its final reference to the [**InkCollector**](inkcollector-class.md) or the [**InkOverlay**](inkoverlay-class.md) object, thus destroying the object, directly from the ink thread.</span></span> <span data-ttu-id="df33c-119">Al contrario, l'applicazione deve rilasciare l'oggetto **InkCollector** o l'oggetto **InkOverlay** da un thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="df33c-119">Instead, the application should release the **InkCollector** or the **InkOverlay** object from an application thread.</span></span>

<span data-ttu-id="df33c-120">**Attenzione:** Un'applicazione contrassegnata come MTA o utilizza FTM, che consente chiamate dirette dal thread di input penna nell'Apartment dell'applicazione, può rilasciare il riferimento finale all'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) direttamente dal thread di input penna. Tuttavia, ciò causa un errore irreversibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="df33c-120">**Caution:** An application that is marked MTA or uses the FTM, which allows direct calls from the ink thread into the application's apartment, can release its final reference to the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object directly from the ink thread; however, this causes unrecoverable application failure.</span></span>

## <a name="event-sinks"></a><span data-ttu-id="df33c-121">Sink di evento</span><span class="sxs-lookup"><span data-stu-id="df33c-121">Event Sinks</span></span>

<span data-ttu-id="df33c-122">Se l'applicazione non usa il servizio FTM e un oggetto e il relativo sink di evento vengono creati in diversi Apartment, l'evento viene eseguito sul thread che gestisce il sink di evento.</span><span class="sxs-lookup"><span data-stu-id="df33c-122">If your application is not using the FTM and an object and its event sink are created in different apartments, then the event executes on the thread servicing the event sink.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="df33c-123">Eccezioni nei gestori eventi</span><span class="sxs-lookup"><span data-stu-id="df33c-123">Exceptions within Event Handlers</span></span>

<span data-ttu-id="df33c-124">Le eccezioni generate dall'interno dei gestori di eventi di Tablet PC vengono utilizzate e non sono visibili al resto o all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="df33c-124">Exceptions thrown from within Tablet PC event handlers are consumed and are not visible to the rest or your application.</span></span> <span data-ttu-id="df33c-125">Analogamente, i valori HRESULT non vengono propagati dai gestori di eventi Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="df33c-125">Likewise, HRESULT values are not propagated from Tablet PC event handlers.</span></span> <span data-ttu-id="df33c-126">Se un'applicazione che utilizza il livello COM genera un'eccezione, il thread in background termina e l'eccezione andrà persa.</span><span class="sxs-lookup"><span data-stu-id="df33c-126">If an application using the COM layer throws an exception, the background thread terminates, and the exception will be lost.</span></span> <span data-ttu-id="df33c-127">Non verranno chiamati gestori di eventi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="df33c-127">No additional event handlers will be called.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df33c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df33c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df33c-129">Esempio di sink di evento C++</span><span class="sxs-lookup"><span data-stu-id="df33c-129">C++ Event Sinks Sample</span></span>](c---event-sinks-sample.md)
</dt> <dt>

[<span data-ttu-id="df33c-130">Considerazioni generali sul threading</span><span class="sxs-lookup"><span data-stu-id="df33c-130">General Threading Considerations</span></span>](general-threading-considerations.md)
</dt> <dt>

[<span data-ttu-id="df33c-131">Considerazioni sul threading della libreria gestita</span><span class="sxs-lookup"><span data-stu-id="df33c-131">Managed Library Threading Considerations</span></span>](managed-library-threading-considerations.md)
</dt> </dl>

 

 



