---
title: Media. getItemInfoByAtom, metodo
description: Il metodo getItemInfoByAtom Recupera il valore dell'attributo con il numero di indice specificato.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- Metodo getItemInfoByAtom Windows Media Player
- Metodo getItemInfoByAtom Windows Media Player, classe media
- Media class Media Player Windows, metodo getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332550"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="814ec-106">Media. getItemInfoByAtom, metodo</span><span class="sxs-lookup"><span data-stu-id="814ec-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="814ec-107">Il metodo **getItemInfoByAtom** Recupera il valore dell'attributo con il numero di indice specificato.</span><span class="sxs-lookup"><span data-stu-id="814ec-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="814ec-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="814ec-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="814ec-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="814ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814ec-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="814ec-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="814ec-111">**Numero** (**Long**) che specifica l'indice in corrispondenza del quale si trova un determinato attributo nel set di attributi disponibili.</span><span class="sxs-lookup"><span data-stu-id="814ec-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814ec-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="814ec-112">Return value</span></span>

<span data-ttu-id="814ec-113">Questo metodo restituisce una **stringa** che rappresenta il valore dell'attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="814ec-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="814ec-114">Per gli attributi il cui valore sottostante è **booleano**, viene restituita la stringa "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="814ec-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="814ec-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="814ec-115">Remarks</span></span>

<span data-ttu-id="814ec-116">Questo metodo può essere utilizzato per recuperare i metadati per un elemento multimediale digitale specifico utilizzando un numero di indice dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="814ec-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="814ec-117">È possibile utilizzare la proprietà **attributeCount** per determinare il numero di attributi disponibili per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="814ec-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="814ec-118">Il metodo **getMediaAtom** dell'oggetto **mediacollection** può essere utilizzato anche per recuperare l'indice di un attributo specifico.</span><span class="sxs-lookup"><span data-stu-id="814ec-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="814ec-119">Questa tecnica è in genere più efficiente rispetto ai metodi **GetItemInfo** o **getItemInfoByType** quando si lavora con playlist di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="814ec-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="814ec-120">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="814ec-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="814ec-121">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="814ec-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="814ec-122">Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di [riferimento sull'attributo](attribute-reference.md)Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="814ec-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="814ec-123">**Windows Media Player 10 Mobile:** Gli attributi per un elemento multimediale sono disponibili solo durante la riproduzione, a meno che non vengano recuperati dall'elemento tramite la raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="814ec-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="814ec-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="814ec-124">Requirements</span></span>



| <span data-ttu-id="814ec-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="814ec-125">Requirement</span></span> | <span data-ttu-id="814ec-126">Valore</span><span class="sxs-lookup"><span data-stu-id="814ec-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="814ec-127">Versione</span><span class="sxs-lookup"><span data-stu-id="814ec-127">Version</span></span><br/> | <span data-ttu-id="814ec-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="814ec-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="814ec-129">DLL</span><span class="sxs-lookup"><span data-stu-id="814ec-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="814ec-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="814ec-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814ec-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="814ec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814ec-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="814ec-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="814ec-133">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="814ec-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="814ec-134">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="814ec-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="814ec-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="814ec-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="814ec-136">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="814ec-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="814ec-137">**Mediacollection. getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="814ec-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="814ec-138">**Lettura di valori di attributo**</span><span class="sxs-lookup"><span data-stu-id="814ec-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="814ec-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="814ec-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="814ec-140">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="814ec-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





