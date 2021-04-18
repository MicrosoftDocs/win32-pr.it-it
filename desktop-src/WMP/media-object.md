---
title: Oggetto multimediale
description: L'oggetto multimediale fornisce un modo per specificare o recuperare le proprietà di un elemento multimediale, usando le proprietà e i metodi seguenti.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Media Player di oggetti multimediali di Windows
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299137"
---
# <a name="media-object"></a><span data-ttu-id="14d22-104">Oggetto multimediale</span><span class="sxs-lookup"><span data-stu-id="14d22-104">Media Object</span></span>

<span data-ttu-id="14d22-105">L'oggetto **multimediale** fornisce un modo per specificare o recuperare le proprietà di un elemento multimediale, usando le proprietà e i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="14d22-105">The **Media** object provides a way to specify or retrieve properties of a media item, using the following properties and methods.</span></span>

<span data-ttu-id="14d22-106">L'oggetto **multimediale** supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="14d22-106">The **Media** object supports the following properties.</span></span>



| <span data-ttu-id="14d22-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14d22-107">Property</span></span>                                         | <span data-ttu-id="14d22-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14d22-108">Description</span></span>                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d22-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="14d22-109">attributeCount</span></span>](media-attributecount.md)       | <span data-ttu-id="14d22-110">Recupera il numero di attributi su cui è possibile eseguire query e/o impostare per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14d22-110">Retrieves the number of attributes that can be queried and/or set for the media item.</span></span>              |
| [<span data-ttu-id="14d22-111">duration</span><span class="sxs-lookup"><span data-stu-id="14d22-111">duration</span></span>](media-duration.md)                   | <span data-ttu-id="14d22-112">Recupera la durata in secondi dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="14d22-112">Retrieves the duration in seconds of the current media item.</span></span>                                       |
| [<span data-ttu-id="14d22-113">durationString</span><span class="sxs-lookup"><span data-stu-id="14d22-113">durationString</span></span>](media-durationstring.md)       | <span data-ttu-id="14d22-114">Recupera un valore **stringa** che indica la durata dell'elemento multimediale corrente nel formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="14d22-114">Retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span> |
| [<span data-ttu-id="14d22-115">error</span><span class="sxs-lookup"><span data-stu-id="14d22-115">error</span></span>](media-error.md)                         | <span data-ttu-id="14d22-116">Recupera un oggetto [ErrorItem](erroritem-object.md) se l'elemento multimediale presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="14d22-116">Retrieves an [ErrorItem](erroritem-object.md) object if the media item has an error condition.</span></span>    |
| [<span data-ttu-id="14d22-117">imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="14d22-117">imageSourceHeight</span></span>](media-imagesourceheight.md) | <span data-ttu-id="14d22-118">Recupera l'altezza in pixel dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="14d22-118">Retrieves the height of the current media item in pixels.</span></span>                                          |
| [<span data-ttu-id="14d22-119">imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="14d22-119">imageSourceWidth</span></span>](media-imagesourcewidth.md)   | <span data-ttu-id="14d22-120">Recupera la larghezza dell'elemento multimediale corrente in pixel.</span><span class="sxs-lookup"><span data-stu-id="14d22-120">Retrieves the width of the current media item in pixels.</span></span>                                           |
| [<span data-ttu-id="14d22-121">markerCount</span><span class="sxs-lookup"><span data-stu-id="14d22-121">markerCount</span></span>](media-markercount.md)             | <span data-ttu-id="14d22-122">Recupera il numero di marcatori nell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14d22-122">Retrieves the number of markers in the media item.</span></span>                                                 |
| [<span data-ttu-id="14d22-123">nome</span><span class="sxs-lookup"><span data-stu-id="14d22-123">name</span></span>](media-name.md)                           | <span data-ttu-id="14d22-124">Specifica o Recupera il nome dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14d22-124">Specifies or retrieves the name of the media item.</span></span>                                                 |
| [<span data-ttu-id="14d22-125">sourceURL</span><span class="sxs-lookup"><span data-stu-id="14d22-125">sourceURL</span></span>](media-sourceurl.md)                 | <span data-ttu-id="14d22-126">Recupera l'URL dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14d22-126">Retrieves the URL of the media item.</span></span>                                                               |



 

<span data-ttu-id="14d22-127">L'oggetto **multimediale** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="14d22-127">The **Media** object supports the following methods.</span></span>



| <span data-ttu-id="14d22-128">Metodo</span><span class="sxs-lookup"><span data-stu-id="14d22-128">Method</span></span>                                                       | <span data-ttu-id="14d22-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14d22-129">Description</span></span>                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d22-130">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="14d22-130">getAttributeCountByType</span></span>](media-getattributecountbytype.md) | <span data-ttu-id="14d22-131">Recupera il numero di attributi associati al nome di attributo e alla lingua specificati.</span><span class="sxs-lookup"><span data-stu-id="14d22-131">Retrieves the number of attributes associated with the specified attribute name and language.</span></span>            |
| [<span data-ttu-id="14d22-132">getAttributeName</span><span class="sxs-lookup"><span data-stu-id="14d22-132">getAttributeName</span></span>](media-getattributename.md)               | <span data-ttu-id="14d22-133">Recupera il nome dell'attributo corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="14d22-133">Retrieves the name of the attribute corresponding to the specified index.</span></span>                                |
| [<span data-ttu-id="14d22-134">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="14d22-134">getItemInfo</span></span>](media-getiteminfo.md)                         | <span data-ttu-id="14d22-135">Recupera il valore dell'attributo specificato per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14d22-135">Retrieves the value of the specified attribute for the media item.</span></span>                                       |
| [<span data-ttu-id="14d22-136">getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="14d22-136">getItemInfoByAtom</span></span>](media-getiteminfobyatom.md)             | <span data-ttu-id="14d22-137">Recupera il valore dell'attributo con il numero di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="14d22-137">Retrieves the value of the attribute with the specified index number.</span></span>                                    |
| [<span data-ttu-id="14d22-138">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="14d22-138">getItemInfoByType</span></span>](media-getiteminfobytype.md)             | <span data-ttu-id="14d22-139">Recupera il valore dell'attributo corrispondente al nome dell'attributo, alla lingua e all'indice specificati.</span><span class="sxs-lookup"><span data-stu-id="14d22-139">Retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span> |
| [<span data-ttu-id="14d22-140">getmarcatore</span><span class="sxs-lookup"><span data-stu-id="14d22-140">getMarkerName</span></span>](media-getmarkername.md)                     | <span data-ttu-id="14d22-141">Recupera il nome del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="14d22-141">Retrieves the name of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="14d22-142">getMarkerTime</span><span class="sxs-lookup"><span data-stu-id="14d22-142">getMarkerTime</span></span>](media-getmarkertime.md)                     | <span data-ttu-id="14d22-143">Recupera l'ora del marcatore in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="14d22-143">Retrieves the time of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="14d22-144">Identico</span><span class="sxs-lookup"><span data-stu-id="14d22-144">isIdentical</span></span>](media-isidentical.md)                         | <span data-ttu-id="14d22-145">Recupera un valore che indica se l'oggetto fornito è uguale a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="14d22-145">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                 |
| [<span data-ttu-id="14d22-146">isMemberOf</span><span class="sxs-lookup"><span data-stu-id="14d22-146">isMemberOf</span></span>](media-ismemberof.md)                           | <span data-ttu-id="14d22-147">Recupera un valore che indica se l'elemento multimediale specificato è un membro della playlist specificata.</span><span class="sxs-lookup"><span data-stu-id="14d22-147">Retrieves a value indicating whether the specified media item is a member of the specified playlist.</span></span>     |
| [<span data-ttu-id="14d22-148">isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="14d22-148">isReadOnlyItem</span></span>](media-isreadonlyitem.md)                   | <span data-ttu-id="14d22-149">Recupera un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="14d22-149">Retrieves a value indicating whether the attributes of the specified media item can be edited.</span></span>           |
| [<span data-ttu-id="14d22-150">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="14d22-150">setItemInfo</span></span>](media-setiteminfo.md)                         | <span data-ttu-id="14d22-151">Imposta il valore dell'attributo specificato per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="14d22-151">Sets the value of the specified attribute for the media item.</span></span>                                            |



 

<span data-ttu-id="14d22-152">È possibile accedere all'oggetto **multimediale** tramite le proprietà e i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="14d22-152">The **Media** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="14d22-153">Oggetto</span><span class="sxs-lookup"><span data-stu-id="14d22-153">Object</span></span>                          | <span data-ttu-id="14d22-154">Proprietà o metodo</span><span class="sxs-lookup"><span data-stu-id="14d22-154">Property or method</span></span>                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="14d22-155">Controlli</span><span class="sxs-lookup"><span data-stu-id="14d22-155">Controls</span></span>](controls-object.md) | [<span data-ttu-id="14d22-156">currentItem</span><span class="sxs-lookup"><span data-stu-id="14d22-156">currentItem</span></span>](controls-currentitem.md)                                  |
| [<span data-ttu-id="14d22-157">Player</span><span class="sxs-lookup"><span data-stu-id="14d22-157">Player</span></span>](player-object.md)     | <span data-ttu-id="14d22-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="14d22-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span></span> |
| [<span data-ttu-id="14d22-159">Playlist</span><span class="sxs-lookup"><span data-stu-id="14d22-159">Playlist</span></span>](playlist-object.md) | [<span data-ttu-id="14d22-160">item</span><span class="sxs-lookup"><span data-stu-id="14d22-160">item</span></span>](playlist-item.md)                                                |



 

<span data-ttu-id="14d22-161">Poiché si tratta del mezzo più comune di accesso, *Player*. **currentMedia** viene usato a scopo illustrativo nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="14d22-161">Because it is the most common means of access, *player*.**currentMedia** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="14d22-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14d22-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d22-163">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="14d22-163">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




