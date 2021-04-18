---
title: Mediacollection. sedeleted (metodo)
description: Il metodo sedeleted sposta l'elemento multimediale specificato nella cartella degli elementi eliminati. | Mediacollection. sedeleted (metodo)
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- Metodo sedeleted Media Player Windows
- Metodo sedeleted Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo sedeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327154"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="ab1c8-107">Mediacollection. sedeleted (metodo)</span><span class="sxs-lookup"><span data-stu-id="ab1c8-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="ab1c8-108">Il metodo **Sedeleted** sposta l'elemento multimediale specificato nella cartella degli elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1c8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab1c8-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="ab1c8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab1c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab1c8-111">*elemento* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ab1c8-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1c8-112">Oggetto **multimediale** da spostare.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="ab1c8-113">valore *true* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab1c8-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1c8-114">Specificare sempre questo valore.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab1c8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab1c8-115">Return value</span></span>

<span data-ttu-id="ab1c8-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab1c8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab1c8-117">Remarks</span></span>

<span data-ttu-id="ab1c8-118">Questo metodo non rimuove i file dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="ab1c8-119">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="ab1c8-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ab1c8-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ab1c8-121">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="ab1c8-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="ab1c8-122">Examples</span></span>

<span data-ttu-id="ab1c8-123">Nell'esempio JScript seguente viene utilizzato *mediacollection*. viene **eliminato per spostare** un particolare elemento multimediale, archiviato nella variabile denominata mediaObject, nella cartella Deleted Items.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="ab1c8-124">*Mediacollection*. il metodo **undeleted** verifica prima di tutto se l'elemento è già stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="ab1c8-125">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ab1c8-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="ab1c8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab1c8-126">Requirements</span></span>



| <span data-ttu-id="ab1c8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1c8-127">Requirement</span></span> | <span data-ttu-id="ab1c8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ab1c8-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1c8-129">Versione</span><span class="sxs-lookup"><span data-stu-id="ab1c8-129">Version</span></span><br/> | <span data-ttu-id="ab1c8-130">Windows Media Player versione 7,0, Windows Media Player versione 7,1 o Windows Media Player per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="ab1c8-131">Questo metodo non è supportato per Windows Media Player 9 Series o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ab1c8-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="ab1c8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ab1c8-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab1c8-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab1c8-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="ab1c8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab1c8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1c8-135">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="ab1c8-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ab1c8-136">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="ab1c8-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="ab1c8-137">**Mediacollection. viene eliminato**</span><span class="sxs-lookup"><span data-stu-id="ab1c8-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="ab1c8-138">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ab1c8-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ab1c8-139">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ab1c8-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





