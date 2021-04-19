---
title: Media. getItemInfo, metodo
description: Il metodo getItemInfo Recupera il valore dell'attributo specificato per l'elemento multimediale corrente.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- metodo getItemInfo Windows Media Player
- metodo getItemInfo Windows Media Player, classe media
- Media class Media Player Windows, metodo getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332552"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="6d69c-106">Media. getItemInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="6d69c-106">Media.getItemInfo method</span></span>

<span data-ttu-id="6d69c-107">Il metodo **GetItemInfo** Recupera il valore dell'attributo specificato per l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="6d69c-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d69c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d69c-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="6d69c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d69c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d69c-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d69c-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d69c-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="6d69c-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="6d69c-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6d69c-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d69c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d69c-113">Return value</span></span>

<span data-ttu-id="6d69c-114">Questo metodo restituisce una **stringa** che rappresenta il valore dell'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="6d69c-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="6d69c-115">Per gli attributi il cui valore sottostante è **booleano**, viene restituita la stringa "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="6d69c-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="6d69c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d69c-116">Remarks</span></span>

<span data-ttu-id="6d69c-117">Questo metodo recupera i metadati per un singolo elemento multimediale digitale o un elemento multimediale che fa parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="6d69c-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="6d69c-118">La proprietà **attributeCount** contiene il numero di nomi di attributi disponibili per un determinato oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="6d69c-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="6d69c-119">I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare il nome di ogni attributo disponibile.</span><span class="sxs-lookup"><span data-stu-id="6d69c-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="6d69c-120">I singoli nomi di attributo possono essere passati a **GetItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="6d69c-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="6d69c-121">Per recuperare gli attributi con più valori e attributi con valori complessi, usare il metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="6d69c-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="6d69c-122">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="6d69c-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="6d69c-123">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6d69c-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6d69c-124">Per condividere le librerie di Windows Media tramite UPnP, Windows Media Player crea un servizio directory contenuto (CDS) esposto tramite UPnP.</span><span class="sxs-lookup"><span data-stu-id="6d69c-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="6d69c-125">Gli altri dispositivi potranno quindi navigare ed esplorare le librerie.</span><span class="sxs-lookup"><span data-stu-id="6d69c-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="6d69c-126">In Windows 7, un'applicazione può usare gli attributi Windows Media Player [**TrackingId**](trackingid-attribute.md) e [**mediaType**](mediatype-attribute.md) per costruire l'ID oggetto di ogni elemento in CDS.</span><span class="sxs-lookup"><span data-stu-id="6d69c-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="6d69c-127">Si noti che questa costruzione potrebbe cambiare nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="6d69c-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="6d69c-128">L'applicazione passa ogni stringa di attributo nel parametro *Name* in una chiamata a **GetItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="6d69c-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="6d69c-129">**GetItemInfo** restituisce il valore per ogni attributo nel valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6d69c-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="6d69c-130">L'applicazione usa quindi la sintassi seguente per costruire ogni ID oggetto:</span><span class="sxs-lookup"><span data-stu-id="6d69c-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="6d69c-131">*TrackingId*. 0. *MediaTypeID*</span><span class="sxs-lookup"><span data-stu-id="6d69c-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="6d69c-132">Questa sintassi ha il significato seguente:</span><span class="sxs-lookup"><span data-stu-id="6d69c-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="6d69c-133">*TrackingId* è la stringa archiviata nell'attributo Windows Media Player [**TrackingId**](trackingid-attribute.md) dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="6d69c-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="6d69c-134">*MediaTypeID* dipende dal valore dell'attributo [**mediaType**](mediatype-attribute.md) , come illustrato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="6d69c-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="6d69c-135">Attributo MediaType</span><span class="sxs-lookup"><span data-stu-id="6d69c-135">MediaType attribute</span></span>                      | <span data-ttu-id="6d69c-136">MediaTypeID</span><span class="sxs-lookup"><span data-stu-id="6d69c-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="6d69c-137">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="6d69c-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="6d69c-138">4</span><span class="sxs-lookup"><span data-stu-id="6d69c-138">4</span></span>           |
    | [<span data-ttu-id="6d69c-139">Elementi foto</span><span class="sxs-lookup"><span data-stu-id="6d69c-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="6d69c-140">B</span><span class="sxs-lookup"><span data-stu-id="6d69c-140">B</span></span>           |
    | [<span data-ttu-id="6d69c-141">Elementi video</span><span class="sxs-lookup"><span data-stu-id="6d69c-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="6d69c-142">8</span><span class="sxs-lookup"><span data-stu-id="6d69c-142">8</span></span>           |

    

     

<span data-ttu-id="6d69c-143">**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="6d69c-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d69c-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d69c-144">Requirements</span></span>



| <span data-ttu-id="6d69c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d69c-145">Requirement</span></span> | <span data-ttu-id="6d69c-146">Valore</span><span class="sxs-lookup"><span data-stu-id="6d69c-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d69c-147">Versione</span><span class="sxs-lookup"><span data-stu-id="6d69c-147">Version</span></span><br/> | <span data-ttu-id="6d69c-148">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6d69c-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6d69c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6d69c-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d69c-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d69c-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d69c-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d69c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d69c-152">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="6d69c-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6d69c-153">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="6d69c-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="6d69c-154">**Media. GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="6d69c-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="6d69c-155">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="6d69c-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="6d69c-156">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="6d69c-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="6d69c-157">**Lettura di valori di attributo**</span><span class="sxs-lookup"><span data-stu-id="6d69c-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="6d69c-158">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6d69c-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6d69c-159">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6d69c-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





