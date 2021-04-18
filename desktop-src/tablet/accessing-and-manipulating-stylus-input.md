---
description: Il Tablet PC include la tecnologia per l'interazione con i dati della penna del tablet mentre vengono raccolti.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Accesso e modifica dell'input dello stilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305363"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="d8994-103">Accesso e modifica dell'input dello stilo</span><span class="sxs-lookup"><span data-stu-id="d8994-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="d8994-104">Il Tablet PC include la tecnologia per l'interazione con i dati della penna del tablet mentre vengono raccolti.</span><span class="sxs-lookup"><span data-stu-id="d8994-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="d8994-105">La classe [**RealTimeStylus**](realtimestylus-class.md) fa parte dell'API (Application Programming Interface) di StylusInput, che fornisce l'accesso al flusso di dati della penna del tablet.</span><span class="sxs-lookup"><span data-stu-id="d8994-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="d8994-106">Queste API consentono di acquisire, interrompere e modificare il flusso in modo indipendente dal rendering e dalla raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="d8994-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="d8994-107">Le API StylusInput sono progettate per:</span><span class="sxs-lookup"><span data-stu-id="d8994-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="d8994-108">Fornire l'accesso in tempo reale al flusso di dati della penna del tablet.</span><span class="sxs-lookup"><span data-stu-id="d8994-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="d8994-109">Impedire al thread dell'interfaccia utente di bloccare il rendering dinamico degli input penna accodando i dati dei pacchetti nel thread dell'interfaccia utente e creando una raccolta di input penna a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="d8994-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="d8994-110">Aumentare le prestazioni e ridurre l'utilizzo complessivo dei thread rispetto all'utilizzo dell'oggetto [**InkCollector**](inkcollector-class.md) , dell'oggetto [**InkOverlay**](inkoverlay-class.md) , del controllo [InkPicture](inkpicture-control-reference.md) o del controllo [InkEdit](inkedit-control-reference.md) per raccogliere input penna.</span><span class="sxs-lookup"><span data-stu-id="d8994-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="d8994-111">Le API StylusInput non sono progettate per funzionare con l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) , il controllo [InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d8994-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="d8994-112">Quando è necessario interagire direttamente con il flusso di dati della penna del tablet o quando l'applicazione può bloccare l'Inking in tempo reale, usare l'oggetto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d8994-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="d8994-113">Utilizzare l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) , il controllo [InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) quando il comportamento predefinito di questi oggetti fornisce il comportamento necessario.</span><span class="sxs-lookup"><span data-stu-id="d8994-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d8994-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d8994-114">In This Section</span></span>

<span data-ttu-id="d8994-115">Le sezioni seguenti descrivono gli elementi delle API StylusInput:</span><span class="sxs-lookup"><span data-stu-id="d8994-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="d8994-116">Architettura delle API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="d8994-117">Uso delle API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="d8994-118">Uso della classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="d8994-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="d8994-119">Plug-in e classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="d8994-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="d8994-120">Dati plug-in e classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="d8994-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="d8994-121">Note sull'implementazione per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="d8994-122">Plug-in per la raccolta di input penna</span><span class="sxs-lookup"><span data-stu-id="d8994-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="d8994-123">Plug-in di renderer dinamici</span><span class="sxs-lookup"><span data-stu-id="d8994-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="d8994-124">Plug-in di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="d8994-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="d8994-125">Considerazioni sull'uso delle API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="d8994-126">Considerazioni di progettazione per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="d8994-127">Considerazioni relative al threading per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="d8994-128">Modello di RealTimeStylus a cascata</span><span class="sxs-lookup"><span data-stu-id="d8994-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="d8994-129">Considerazioni sulla gestione degli errori per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="d8994-130">Considerazioni sulle prestazioni per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="d8994-131">Considerazioni sull'attendibilità parziale per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="d8994-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="d8994-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8994-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8994-133">Esempio di plug-in RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="d8994-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="d8994-134">Esempio di raccolta inchiostro RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="d8994-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



