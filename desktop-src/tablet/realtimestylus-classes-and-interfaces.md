---
description: Questa sezione contiene informazioni sulle interfacce e sulle classi usate nello stilo in tempo reale.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Classi e interfacce RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882777"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="00a57-103">Classi e interfacce RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="00a57-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="00a57-104">Questa sezione contiene informazioni sulle interfacce e sulle classi usate nello stilo in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="00a57-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="00a57-105">Le interfacce e le classi stilo in tempo reale non sono conformi all'automazione.</span><span class="sxs-lookup"><span data-stu-id="00a57-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="00a57-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="00a57-106">In This Section</span></span>



| <span data-ttu-id="00a57-107">Classe</span><span class="sxs-lookup"><span data-stu-id="00a57-107">Class</span></span>                                                      | <span data-ttu-id="00a57-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00a57-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00a57-109">**Classe RealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="00a57-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="00a57-110">Implementa l'interfaccia [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="00a57-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="00a57-111">[**Classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00a57-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="00a57-112">Implementa l'interfaccia dell' [**interfaccia IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .</span><span class="sxs-lookup"><span data-stu-id="00a57-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="00a57-113">**Classe GestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="00a57-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="00a57-114">Implementa l'interfaccia dell' [**interfaccia IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .</span><span class="sxs-lookup"><span data-stu-id="00a57-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="00a57-115">**Classe StrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="00a57-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="00a57-116">Implementa l'interfaccia dell' [**interfaccia IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .</span><span class="sxs-lookup"><span data-stu-id="00a57-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="00a57-117">Interfacce</span><span class="sxs-lookup"><span data-stu-id="00a57-117">Interfaces</span></span>



| <span data-ttu-id="00a57-118">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="00a57-118">Interface</span></span>                                                                          | <span data-ttu-id="00a57-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00a57-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00a57-120">**Interfaccia IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="00a57-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="00a57-121">Espone metodi che consentono di controllare la visualizzazione dei dati dello stilo in tempo reale poiché i dati vengono gestiti dall'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="00a57-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="00a57-122">**Interfaccia IGestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="00a57-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="00a57-123">Espone metodi che consentono di reagire agli eventi riconoscendo i movimenti dello stilo e consentendo di aggiungere dati alla coda di input.</span><span class="sxs-lookup"><span data-stu-id="00a57-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="00a57-124">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="00a57-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="00a57-125">Gestisce i dati del pacchetto dello stilo da un digitalizzatore in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="00a57-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="00a57-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="00a57-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="00a57-127">Estende l'interfaccia IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="00a57-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="00a57-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="00a57-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="00a57-129">Estende l'interfaccia IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="00a57-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="00a57-130">**Interfaccia IRealTimeStylusSynchronization**</span><span class="sxs-lookup"><span data-stu-id="00a57-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="00a57-131">Sincronizza l'accesso all'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="00a57-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="00a57-132">**Interfaccia IStrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="00a57-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="00a57-133">Espone metodi che consentono di creare tratti a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="00a57-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="00a57-134">**Interfaccia IStylusPlugin**</span><span class="sxs-lookup"><span data-stu-id="00a57-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="00a57-135">Espone metodi che consentono di ricevere notifiche di eventi e di eseguire l'elaborazione personalizzata in base a tali eventi.</span><span class="sxs-lookup"><span data-stu-id="00a57-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="00a57-136">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="00a57-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="00a57-137">Rappresenta un plug-in asincrono che può essere aggiunto alla raccolta di plug-in asincrona della [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="00a57-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="00a57-138">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="00a57-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="00a57-139">Rappresenta un plug-in sincrono che può essere aggiunto alla raccolta di plug-in sincrona della [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="00a57-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="00a57-140">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="00a57-140">Return Values</span></span>

<span data-ttu-id="00a57-141">I metodi nella libreria COM restituiscono valori **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="00a57-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="00a57-142">Se non specificato diversamente, i significati dei valori **HRESULT** sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="00a57-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="00a57-143">Valore HRESULT</span><span class="sxs-lookup"><span data-stu-id="00a57-143">HRESULT value</span></span>                                   | <span data-ttu-id="00a57-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00a57-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a57-145">\_OK</span><span class="sxs-lookup"><span data-stu-id="00a57-145">S\_OK</span></span><br/>                                | <span data-ttu-id="00a57-146">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="00a57-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="00a57-147">\_puntatore E</span><span class="sxs-lookup"><span data-stu-id="00a57-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="00a57-148">Almeno un puntatore (per un parametro di input o di output) non è valido.</span><span class="sxs-lookup"><span data-stu-id="00a57-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="00a57-149">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="00a57-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="00a57-150">Il membro ha tentato di passare un argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="00a57-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="00a57-151">E \_ \_ eccezione Ink</span><span class="sxs-lookup"><span data-stu-id="00a57-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="00a57-152">Si è verificata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="00a57-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="00a57-153">E \_ OutOfMemory</span><span class="sxs-lookup"><span data-stu-id="00a57-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="00a57-154">Il sistema non è in grado di allocare memoria per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="00a57-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="00a57-155">E \_ non riescono</span><span class="sxs-lookup"><span data-stu-id="00a57-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="00a57-156">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="00a57-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="00a57-157">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="00a57-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="00a57-158">Il membro ha tentato di usare un'operazione non valida.</span><span class="sxs-lookup"><span data-stu-id="00a57-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="00a57-159">\_modalità TPC E \_ non valida \_</span><span class="sxs-lookup"><span data-stu-id="00a57-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="00a57-160">Il membro ha tentato di usare una modalità non valida.</span><span class="sxs-lookup"><span data-stu-id="00a57-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="00a57-161">\_configurazione TPC E \_ non valida \_</span><span class="sxs-lookup"><span data-stu-id="00a57-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="00a57-162">Il membro ha tentato di usare una configurazione non valida.</span><span class="sxs-lookup"><span data-stu-id="00a57-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="00a57-163">\_Descrizione pacchetto TPC E \_ non valida \_ \_</span><span class="sxs-lookup"><span data-stu-id="00a57-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="00a57-164">Il membro ha tentato di usare una descrizione del pacchetto non valida.</span><span class="sxs-lookup"><span data-stu-id="00a57-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="00a57-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00a57-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00a57-166">Riferimento a RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="00a57-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
