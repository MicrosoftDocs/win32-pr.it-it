---
title: Mediacollection. Metodo eliminato
description: Il metodo IsValid recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella Deleted Items.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- Metodo eliminato Media Player Windows
- Metodo di eliminazione di Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo eliminato
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327162"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="c620c-106">Mediacollection. Metodo eliminato</span><span class="sxs-lookup"><span data-stu-id="c620c-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="c620c-107">Il **Metodo IsValid** recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella Deleted Items.</span><span class="sxs-lookup"><span data-stu-id="c620c-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c620c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c620c-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="c620c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c620c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c620c-110">*elemento* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c620c-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c620c-111">Oggetto **multimediale** che può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="c620c-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c620c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c620c-112">Return value</span></span>

<span data-ttu-id="c620c-113">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="c620c-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c620c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c620c-114">Remarks</span></span>

<span data-ttu-id="c620c-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c620c-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c620c-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c620c-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c620c-117">**Windows Media Player 10 Mobile:** Questo metodo restituisce sempre **false**.</span><span class="sxs-lookup"><span data-stu-id="c620c-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="c620c-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="c620c-118">Examples</span></span>

<span data-ttu-id="c620c-119">Nell'esempio JScript seguente viene utilizzato *mediacollection*. viene **eliminato per verificare** se un particolare elemento multimediale, archiviato nella variabile denominata mediaObject, si trova nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="c620c-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="c620c-120">Se l'elemento multimediale non è già stato eliminato, viene spostato nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="c620c-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="c620c-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c620c-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="c620c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c620c-122">Requirements</span></span>



| <span data-ttu-id="c620c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c620c-123">Requirement</span></span> | <span data-ttu-id="c620c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c620c-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c620c-125">Versione</span><span class="sxs-lookup"><span data-stu-id="c620c-125">Version</span></span><br/> | <span data-ttu-id="c620c-126">Windows Media Player versione 7,0, Windows Media Player versione 7,1 o Windows Media Player per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c620c-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="c620c-127">Questo metodo non è supportato per Windows Media Player 9 Series o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c620c-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="c620c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c620c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c620c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c620c-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="c620c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c620c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c620c-131">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="c620c-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c620c-132">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="c620c-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c620c-133">**Mediacollection. sedeleted**</span><span class="sxs-lookup"><span data-stu-id="c620c-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="c620c-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c620c-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c620c-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c620c-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





