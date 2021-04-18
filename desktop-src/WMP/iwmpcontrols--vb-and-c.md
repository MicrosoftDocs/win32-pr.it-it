---
title: Interfaccia IWMPControls (VB e C) (WMP. h)
description: Consente di modificare la riproduzione di un elemento multimediale rappresentando i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause. l'interfaccia IWMPControls espone le proprietà seguenti.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Interfaccia IWMPControls (VB e C) Windows Media Player
- Interfaccia IWMPControls (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328216"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a><span data-ttu-id="a4283-105">Interfaccia IWMPControls (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="a4283-105">IWMPControls (VB and C#) interface</span></span>

<span data-ttu-id="a4283-106">Consente di modificare la riproduzione di un elemento multimediale rappresentando i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause.</span><span class="sxs-lookup"><span data-stu-id="a4283-106">Provides a way to manipulate the playback of a media item by representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>

<span data-ttu-id="a4283-107">L'interfaccia **IWMPControls** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="a4283-107">The **IWMPControls** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="a4283-108">Membri</span><span class="sxs-lookup"><span data-stu-id="a4283-108">Members</span></span>

<span data-ttu-id="a4283-109">L'interfaccia **IWMPControls (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a4283-109">The **IWMPControls (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="a4283-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4283-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4283-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4283-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4283-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4283-112">Methods</span></span>

<span data-ttu-id="a4283-113">L'interfaccia **IWMPControls (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a4283-113">The **IWMPControls (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="a4283-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a4283-114">Method</span></span>                                                                       | <span data-ttu-id="a4283-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4283-115">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4283-116">**fastForward**</span><span class="sxs-lookup"><span data-stu-id="a4283-116">**fastForward**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | <span data-ttu-id="a4283-117">Avvia la riproduzione veloce dell'elemento multimediale nella direzione in avanti.</span><span class="sxs-lookup"><span data-stu-id="a4283-117">Starts fast play of the media item in the forward direction.</span></span><br/>                     |
| [<span data-ttu-id="a4283-118">**fastReverse**</span><span class="sxs-lookup"><span data-stu-id="a4283-118">**fastReverse**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | <span data-ttu-id="a4283-119">Avvia la riproduzione veloce dell'elemento multimediale nella direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="a4283-119">Starts fast play of the media item in the reverse direction.</span></span><br/>                     |
| [<span data-ttu-id="a4283-120">**prossimo**</span><span class="sxs-lookup"><span data-stu-id="a4283-120">**next**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | <span data-ttu-id="a4283-121">Imposta l'elemento successivo nella playlist come elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="a4283-121">Sets the next item in the playlist as the current item.</span></span><br/>                          |
| [<span data-ttu-id="a4283-122">**pause**</span><span class="sxs-lookup"><span data-stu-id="a4283-122">**pause**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | <span data-ttu-id="a4283-123">Sospende la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4283-123">Pauses playback of the media item.</span></span><br/>                                               |
| [<span data-ttu-id="a4283-124">**Play**</span><span class="sxs-lookup"><span data-stu-id="a4283-124">**play**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | <span data-ttu-id="a4283-125">Inizia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.</span><span class="sxs-lookup"><span data-stu-id="a4283-125">Begins playback of the current media item, or resumes playback of a paused item.</span></span><br/> |
| [<span data-ttu-id="a4283-126">**playItem**</span><span class="sxs-lookup"><span data-stu-id="a4283-126">**playItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | <span data-ttu-id="a4283-127">Riproduce l'elemento multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="a4283-127">Plays the specified media item.</span></span><br/>                                                  |
| [<span data-ttu-id="a4283-128">**precedente**</span><span class="sxs-lookup"><span data-stu-id="a4283-128">**previous**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | <span data-ttu-id="a4283-129">Imposta l'elemento precedente nella playlist come elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="a4283-129">Sets the previous item in the playlist as the current item.</span></span><br/>                      |
| [<span data-ttu-id="a4283-130">**arrestare**</span><span class="sxs-lookup"><span data-stu-id="a4283-130">**stop**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | <span data-ttu-id="a4283-131">Interrompe la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4283-131">Stops playback of the media item.</span></span><br/>                                                |



 

### <a name="properties"></a><span data-ttu-id="a4283-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4283-132">Properties</span></span>

<span data-ttu-id="a4283-133">L'interfaccia **IWMPControls (VB e C#)** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4283-133">The **IWMPControls (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="a4283-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4283-134">Property</span></span>                                                                                                    | <span data-ttu-id="a4283-135">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a4283-135">Access type</span></span>           | <span data-ttu-id="a4283-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4283-136">Description</span></span>                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4283-137">**currentItem**</span><span class="sxs-lookup"><span data-stu-id="a4283-137">**currentItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | <span data-ttu-id="a4283-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a4283-138">Read/write</span></span><br/> | <span data-ttu-id="a4283-139">Ottiene o imposta l'elemento multimediale corrente in una playlist.</span><span class="sxs-lookup"><span data-stu-id="a4283-139">Gets or sets the current media item in a playlist.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="a4283-140">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="a4283-140">**currentMarker**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | <span data-ttu-id="a4283-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a4283-141">Read/write</span></span><br/> | <span data-ttu-id="a4283-142">Ottiene o imposta il numero dell'indicatore corrente.</span><span class="sxs-lookup"><span data-stu-id="a4283-142">Gets or sets the current marker number.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="a4283-143">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="a4283-143">**currentPosition**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | <span data-ttu-id="a4283-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a4283-144">Read/write</span></span><br/> | <span data-ttu-id="a4283-145">Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="a4283-145">Gets or sets the current position in the media item in seconds from the beginning.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a4283-146">**currentPositionString**</span><span class="sxs-lookup"><span data-stu-id="a4283-146">**currentPositionString**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | <span data-ttu-id="a4283-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4283-147">Read-only</span></span><br/>  | <span data-ttu-id="a4283-148">Ottiene la posizione corrente nell'elemento multimediale come **System. String**.</span><span class="sxs-lookup"><span data-stu-id="a4283-148">Gets the current position in the media item as a **System.String**.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a4283-149">**isAvailable**</span><span class="sxs-lookup"><span data-stu-id="a4283-149">**isAvailable**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | <span data-ttu-id="a4283-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4283-150">Read-only</span></span><br/>  | <span data-ttu-id="a4283-151">Ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.</span><span class="sxs-lookup"><span data-stu-id="a4283-151">Gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span> <span data-ttu-id="a4283-152">In C# si tratta del metodo **get \_ unavailable** .</span><span class="sxs-lookup"><span data-stu-id="a4283-152">In C#, this is the **get\_isAvailable** method.</span></span><br/> |



 

<span data-ttu-id="a4283-153">Ottenere un'interfaccia **IWMPControls** usando la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="a4283-153">Get an **IWMPControls** interface by using the following property.</span></span>



| <span data-ttu-id="a4283-154">Oggetto</span><span class="sxs-lookup"><span data-stu-id="a4283-154">Object</span></span>                                                                   | <span data-ttu-id="a4283-155">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4283-155">Property</span></span>                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a4283-156">Oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a4283-156">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="a4283-157">**Ctlcontrols**</span><span class="sxs-lookup"><span data-stu-id="a4283-157">**Ctlcontrols**</span></span>](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="a4283-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4283-158">Requirements</span></span>



| <span data-ttu-id="a4283-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4283-159">Requirement</span></span> | <span data-ttu-id="a4283-160">Valore</span><span class="sxs-lookup"><span data-stu-id="a4283-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a4283-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4283-161">Header</span></span><br/> | <dl> <span data-ttu-id="a4283-162"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4283-162"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4283-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4283-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4283-164">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="a4283-164">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4283-165">**Interfaccia IWMPControls2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4283-165">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4283-166">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a4283-166">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





