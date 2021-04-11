---
description: Consente di accedere agli eventi dello stilo provenienti dai digitalizzatori penna o touch.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Riferimento a RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232477"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="f3645-103">Riferimento a RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f3645-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="f3645-104">Consente di accedere agli eventi dello stilo provenienti dai digitalizzatori penna o touch.</span><span class="sxs-lookup"><span data-stu-id="f3645-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3645-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f3645-105">In This Section</span></span>

-   [<span data-ttu-id="f3645-106">Classi e interfacce RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f3645-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="f3645-107">Enumerazioni RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f3645-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="f3645-108">Strutture RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f3645-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="f3645-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3645-109">Remarks</span></span>

<span data-ttu-id="f3645-110">Questo oggetto implementa l'interfaccia com [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="f3645-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="f3645-111">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="f3645-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="f3645-112">È possibile controllare completamente, eseguire dinamicamente il rendering, modificare e persino eliminare dati dal flusso di pacchetti all'interno dei plug-in sincroni e asincroni dell'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f3645-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="f3645-113">Lo stilo in tempo reale fornisce un modo per creare un oggetto **InkCollecting** a thread singolo e residente nel thread dell'interfaccia utente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f3645-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="f3645-114">Questo oggetto **InkCollecting** accede ai dati dello stilo in tempo reale dalla coda.</span><span class="sxs-lookup"><span data-stu-id="f3645-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="f3645-115">Un oggetto **InkCollecting** insieme a stilo in tempo reale consente la modifica in tempo reale della selezione e la modifica in tempo reale dei dati Ink raccolti.</span><span class="sxs-lookup"><span data-stu-id="f3645-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="f3645-116">Per ulteriori informazioni, vedere [accesso e modifica dell'input dello stilo](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="f3645-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="f3645-117">Usare l'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) per interagire direttamente con il flusso di dati dello stilo del tablet o per bloccare l'Inking in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="f3645-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="f3645-118">Utilizzare l'oggetto [**classe InkCollector**](inkcollector-class.md) , l'oggetto [**classe InkOverlay**](inkoverlay-class.md) , il controllo di [controllo InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) quando il comportamento predefinito di questi oggetti fornisce il comportamento necessario.</span><span class="sxs-lookup"><span data-stu-id="f3645-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="f3645-119">Gli eventi dello stilo in tempo reale si trovano in un handle di finestra specifico all'interno di un rettangolo di input della finestra specifico.</span><span class="sxs-lookup"><span data-stu-id="f3645-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="f3645-120">RealTimeStylusService può inviare dati dello stilo a più oggetti [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f3645-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="f3645-121">Ogni oggetto **classe RealTimeStylus** riceve i dati dello stilo per una sezione specifica di una finestra basata sulla [**Proprietà IRealTimeStylus:: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definita per l'oggetto **classe RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="f3645-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="f3645-122">L'oggetto **classe RealTimeStylus** ottiene i dati dello stilo e quindi li elabora tramite un elenco di plug-in sincroni e asincroni.</span><span class="sxs-lookup"><span data-stu-id="f3645-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="f3645-123">La differenza tra i plug-in sincroni e i plug-in asincroni risiede nel thread in cui vengono eseguiti e nella sequenza chiamante.</span><span class="sxs-lookup"><span data-stu-id="f3645-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="f3645-124">I plug-in sincroni vengono chiamati dal thread in cui viene eseguito l'oggetto [**RealTimeStylus Class**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f3645-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="f3645-125">Ogni volta che viene creata un'istanza dell'oggetto **classe RealTimeStylus** , viene creata un'istanza di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f3645-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="f3645-126">I plug-in sincroni vengono eseguiti sul nuovo thread di cui è stata creata un'istanza per l'istanza dell'oggetto **classe RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="f3645-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="f3645-127">I plug-in asincroni vengono chiamati tramite l'interfaccia utente o il thread dell'applicazione dopo che il flusso di pacchetti è stato elaborato dai plug-in sincroni e archiviato nella coda di output.</span><span class="sxs-lookup"><span data-stu-id="f3645-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3645-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3645-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3645-129">**Interfaccia IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="f3645-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="f3645-130">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="f3645-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="f3645-131">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="f3645-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="f3645-132">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="f3645-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
