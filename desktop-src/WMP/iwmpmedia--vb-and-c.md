---
title: Interfaccia IWMPMedia (VB e C) (WMP. h)
description: Consente di impostare e recuperare le proprietà di un elemento multimediale. L'interfaccia IWMPMedia espone le proprietà seguenti.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- Interfaccia IWMPMedia (VB e C) Windows Media Player
- Interfaccia IWMPMedia (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331391"
---
# <a name="iwmpmedia-vb-and-c-interface"></a><span data-ttu-id="d77d1-105">Interfaccia IWMPMedia (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="d77d1-105">IWMPMedia (VB and C#) interface</span></span>

<span data-ttu-id="d77d1-106">Consente di impostare e recuperare le proprietà di un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-106">Provides a way to set and retrieve the properties of a media item.</span></span>

<span data-ttu-id="d77d1-107">L'interfaccia **IWMPMedia** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="d77d1-107">The **IWMPMedia** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="d77d1-108">Membri</span><span class="sxs-lookup"><span data-stu-id="d77d1-108">Members</span></span>

<span data-ttu-id="d77d1-109">L'interfaccia **IWMPMedia (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d77d1-109">The **IWMPMedia (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="d77d1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="d77d1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d77d1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d77d1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d77d1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="d77d1-112">Methods</span></span>

<span data-ttu-id="d77d1-113">L'interfaccia **IWMPMedia (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d77d1-113">The **IWMPMedia (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="d77d1-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="d77d1-114">Method</span></span>                                                                             | <span data-ttu-id="d77d1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d77d1-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d77d1-116">**getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="d77d1-116">**getAttributeName**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | <span data-ttu-id="d77d1-117">Restituisce il nome dell'attributo corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d77d1-117">Returns the name of the attribute corresponding to the specified index.</span></span><br/>                            |
| [<span data-ttu-id="d77d1-118">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="d77d1-118">**getItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | <span data-ttu-id="d77d1-119">Restituisce il valore dell'attributo specificato per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-119">Returns the value of the specified attribute for the media item.</span></span><br/>                                   |
| [<span data-ttu-id="d77d1-120">**getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="d77d1-120">**getItemInfoByAtom**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | <span data-ttu-id="d77d1-121">Restituisce il valore dell'attributo con il numero di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d77d1-121">Returns the value of the attribute with the specified index number.</span></span><br/>                                |
| [<span data-ttu-id="d77d1-122">**getmarcatore**</span><span class="sxs-lookup"><span data-stu-id="d77d1-122">**getMarkerName**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | <span data-ttu-id="d77d1-123">Restituisce il nome del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d77d1-123">Returns the name of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="d77d1-124">**getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="d77d1-124">**getMarkerTime**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | <span data-ttu-id="d77d1-125">Restituisce l'ora del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d77d1-125">Returns the time of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="d77d1-126">**isMemberOf**</span><span class="sxs-lookup"><span data-stu-id="d77d1-126">**isMemberOf**</span></span>](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | <span data-ttu-id="d77d1-127">Restituisce un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.</span><span class="sxs-lookup"><span data-stu-id="d77d1-127">Returns a value indicating whether the specified media item is a member of the specified playlist.</span></span><br/> |
| [<span data-ttu-id="d77d1-128">**isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="d77d1-128">**isReadOnlyItem**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | <span data-ttu-id="d77d1-129">Restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="d77d1-129">Returns a value indicating whether the attributes of the specified media item can be edited.</span></span><br/>       |
| [<span data-ttu-id="d77d1-130">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="d77d1-130">**setItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | <span data-ttu-id="d77d1-131">Imposta il valore dell'attributo specificato per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-131">Sets the value of the specified attribute for the media item.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="d77d1-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d77d1-132">Properties</span></span>

<span data-ttu-id="d77d1-133">L'interfaccia **IWMPMedia (VB e C#)** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d77d1-133">The **IWMPMedia (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="d77d1-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d77d1-134">Property</span></span>                                                                                      | <span data-ttu-id="d77d1-135">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d77d1-135">Access type</span></span>          | <span data-ttu-id="d77d1-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d77d1-136">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d77d1-137">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="d77d1-137">**attributeCount**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | <span data-ttu-id="d77d1-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-138">Read-only</span></span><br/> | <span data-ttu-id="d77d1-139">Ottiene il numero di attributi su cui è possibile eseguire query e/o impostare per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-139">Gets the number of attributes that can be queried and/or set for the media item.</span></span><br/>                                                          |
| [<span data-ttu-id="d77d1-140">**durata**</span><span class="sxs-lookup"><span data-stu-id="d77d1-140">**duration**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | <span data-ttu-id="d77d1-141">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-141">Read-only</span></span><br/> | <span data-ttu-id="d77d1-142">Ottiene la durata in secondi dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="d77d1-142">Gets the duration in seconds of the current media item.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d77d1-143">**durationString**</span><span class="sxs-lookup"><span data-stu-id="d77d1-143">**durationString**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | <span data-ttu-id="d77d1-144">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-144">Read-only</span></span><br/> | <span data-ttu-id="d77d1-145">Ottiene un valore che indica la durata dell'elemento multimediale corrente nel formato HH: MM: SS.</span><span class="sxs-lookup"><span data-stu-id="d77d1-145">Gets a value indicating the duration of the current media item in HH:MM:SS format.</span></span><br/>                                                        |
| [<span data-ttu-id="d77d1-146">**imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="d77d1-146">**imageSourceHeight**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | <span data-ttu-id="d77d1-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-147">Read-only</span></span><br/> | <span data-ttu-id="d77d1-148">Ottiene l'altezza in pixel dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="d77d1-148">Gets the height of the current media item in pixels.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d77d1-149">**imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="d77d1-149">**imageSourceWidth**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | <span data-ttu-id="d77d1-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-150">Read-only</span></span><br/> | <span data-ttu-id="d77d1-151">Ottiene la larghezza in pixel dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="d77d1-151">Gets the width of the current media item in pixels.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d77d1-152">**Identico**</span><span class="sxs-lookup"><span data-stu-id="d77d1-152">**isIdentical**</span></span>](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | <span data-ttu-id="d77d1-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-153">Read-only</span></span><br/> | <span data-ttu-id="d77d1-154">Ottiene un valore che indica se l'elemento multimediale specificato è uguale a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="d77d1-154">Gets a value indicating whether the specified media item is the same as the current one.</span></span> <span data-ttu-id="d77d1-155">In C# il metodo Get è **\_ identico** .</span><span class="sxs-lookup"><span data-stu-id="d77d1-155">In C#, this is the **get\_isIdentical** method.</span></span><br/> |
| [<span data-ttu-id="d77d1-156">**markerCount**</span><span class="sxs-lookup"><span data-stu-id="d77d1-156">**markerCount**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | <span data-ttu-id="d77d1-157">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-157">Read-only</span></span><br/> | <span data-ttu-id="d77d1-158">Ottiene il numero di marcatori nell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-158">Gets the number of markers in the media item.</span></span><br/>                                                                                             |
| [<span data-ttu-id="d77d1-159">**nome**</span><span class="sxs-lookup"><span data-stu-id="d77d1-159">**name**</span></span>](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | <span data-ttu-id="d77d1-160">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-160">Read-only</span></span><br/> | <span data-ttu-id="d77d1-161">Ottiene o imposta il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-161">Gets or sets the name of the media item.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="d77d1-162">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="d77d1-162">**sourceURL**</span></span>](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | <span data-ttu-id="d77d1-163">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d77d1-163">Read-only</span></span><br/> | <span data-ttu-id="d77d1-164">Ottiene l'URL dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="d77d1-164">Gets the URL of the media item.</span></span><br/>                                                                                                           |



 

<span data-ttu-id="d77d1-165">Ottenere un'interfaccia **IWMPMedia** usando le proprietà o i metodi seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.</span><span class="sxs-lookup"><span data-stu-id="d77d1-165">Get an **IWMPMedia** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="d77d1-166">Oggetto o interfaccia</span><span class="sxs-lookup"><span data-stu-id="d77d1-166">Object or interface</span></span>                                               | <span data-ttu-id="d77d1-167">Proprietà o metodo</span><span class="sxs-lookup"><span data-stu-id="d77d1-167">Property or method</span></span>                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d77d1-168">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="d77d1-168">**IWMPControls**</span></span>](iwmpcontrols--vb-and-c.md)                    | [<span data-ttu-id="d77d1-169">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="d77d1-169">**currentitem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [<span data-ttu-id="d77d1-170">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d77d1-170">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="d77d1-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="d77d1-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [**newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="d77d1-172">**IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d77d1-172">**IWMPPlaylist**</span></span>](iwmpplaylist--vb-and-c.md)                    | <span data-ttu-id="d77d1-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (Get \_ Item in C#)</span><span class="sxs-lookup"><span data-stu-id="d77d1-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (get\_Item in C#)</span></span>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="d77d1-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d77d1-174">Requirements</span></span>



| <span data-ttu-id="d77d1-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="d77d1-175">Requirement</span></span> | <span data-ttu-id="d77d1-176">Valore</span><span class="sxs-lookup"><span data-stu-id="d77d1-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d77d1-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d77d1-177">Header</span></span><br/> | <dl> <span data-ttu-id="d77d1-178"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d77d1-178"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d77d1-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d77d1-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77d1-180">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="d77d1-180">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="d77d1-181">**Interfaccia IWMPMedia2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d77d1-181">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d77d1-182">**Interfaccia IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d77d1-182">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





