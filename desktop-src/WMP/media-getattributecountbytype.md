---
title: Media. getAttributeCountByType, metodo
description: Il metodo getAttributeCountByType Recupera il numero di attributi associati al nome dell'attributo e alla lingua specificati.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- Metodo getAttributeCountByType Windows Media Player
- Metodo getAttributeCountByType Windows Media Player, classe media
- Media class Media Player Windows, metodo getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332554"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="75ae5-106">Media. getAttributeCountByType, metodo</span><span class="sxs-lookup"><span data-stu-id="75ae5-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="75ae5-107">Il metodo **getAttributeCountByType** Recupera il numero di attributi associati al nome dell'attributo e alla lingua specificati.</span><span class="sxs-lookup"><span data-stu-id="75ae5-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ae5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75ae5-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="75ae5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="75ae5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ae5-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75ae5-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ae5-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="75ae5-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="75ae5-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="75ae5-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="75ae5-113">*lingua* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="75ae5-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ae5-114">**Stringa** che rappresenta la lingua.</span><span class="sxs-lookup"><span data-stu-id="75ae5-114">**String** representing the language.</span></span> <span data-ttu-id="75ae5-115">Se il valore è impostato su null o su "" (stringa vuota), viene utilizzata la stringa delle impostazioni locali corrente.</span><span class="sxs-lookup"><span data-stu-id="75ae5-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="75ae5-116">In caso contrario, il valore deve essere una stringa di linguaggio RFC 1766 valida, ad esempio "en-US".</span><span class="sxs-lookup"><span data-stu-id="75ae5-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ae5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75ae5-117">Return value</span></span>

<span data-ttu-id="75ae5-118">Questo metodo restituisce un **numero** (**Long**) che contiene il numero di attributi.</span><span class="sxs-lookup"><span data-stu-id="75ae5-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ae5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ae5-119">Remarks</span></span>

<span data-ttu-id="75ae5-120">Questo metodo viene utilizzato per determinare il numero di attributi corrispondenti a un nome di attributo specifico per un determinato oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="75ae5-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="75ae5-121">I numeri di indice possono quindi essere passati al metodo **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="75ae5-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="75ae5-122">Questa operazione è utile, ad esempio, quando un elemento multimediale è stato categorizzato in più generi.</span><span class="sxs-lookup"><span data-stu-id="75ae5-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="75ae5-123">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="75ae5-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="75ae5-124">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="75ae5-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="75ae5-125">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.</span><span class="sxs-lookup"><span data-stu-id="75ae5-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ae5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75ae5-126">Requirements</span></span>



| <span data-ttu-id="75ae5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ae5-127">Requirement</span></span> | <span data-ttu-id="75ae5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="75ae5-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75ae5-129">Versione</span><span class="sxs-lookup"><span data-stu-id="75ae5-129">Version</span></span><br/> | <span data-ttu-id="75ae5-130">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="75ae5-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="75ae5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="75ae5-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="75ae5-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ae5-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ae5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75ae5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ae5-134">**MediaObject**</span><span class="sxs-lookup"><span data-stu-id="75ae5-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="75ae5-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="75ae5-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="75ae5-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="75ae5-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="75ae5-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="75ae5-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





