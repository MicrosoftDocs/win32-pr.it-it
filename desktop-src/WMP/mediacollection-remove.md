---
title: Metodo mediacollection. Remove
description: Il metodo Remove rimuove un elemento dall'insieme di supporti.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- rimuovere il metodo Windows Media Player
- Metodo Remove Media Player Windows, classe Mediacollection
- Mediacollection (classe) Windows Media Player, Remove (metodo)
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327161"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="7d809-106">Metodo mediacollection. Remove</span><span class="sxs-lookup"><span data-stu-id="7d809-106">MediaCollection.remove method</span></span>

<span data-ttu-id="7d809-107">Il metodo **Remove** rimuove un elemento dall'insieme di supporti.</span><span class="sxs-lookup"><span data-stu-id="7d809-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d809-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d809-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="7d809-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d809-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d809-110">*elemento* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7d809-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d809-111">Oggetto **multimediale** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7d809-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="7d809-112">*Elimina* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d809-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d809-113">**Valore booleano** che indica se rimuovere l'elemento.</span><span class="sxs-lookup"><span data-stu-id="7d809-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d809-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d809-114">Return value</span></span>

<span data-ttu-id="7d809-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7d809-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d809-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d809-116">Remarks</span></span>

<span data-ttu-id="7d809-117">Questo metodo elimina un elemento dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="7d809-117">This method deletes an item from the library.</span></span> <span data-ttu-id="7d809-118">Questo metodo non elimina i file dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7d809-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="7d809-119">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="7d809-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="7d809-120">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7d809-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7d809-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="7d809-121">Examples</span></span>

<span data-ttu-id="7d809-122">Il seguente esempio di JScript, dopo la richiesta all'utente, Elimina definitivamente il primo elemento multimediale della raccolta di supporti usando *mediacollection*. **rimuovere**.</span><span class="sxs-lookup"><span data-stu-id="7d809-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="7d809-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7d809-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="7d809-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d809-124">Requirements</span></span>



| <span data-ttu-id="7d809-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d809-125">Requirement</span></span> | <span data-ttu-id="7d809-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7d809-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d809-127">Versione</span><span class="sxs-lookup"><span data-stu-id="7d809-127">Version</span></span><br/> | <span data-ttu-id="7d809-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="7d809-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7d809-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7d809-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d809-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d809-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d809-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d809-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d809-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="7d809-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7d809-133">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="7d809-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7d809-134">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="7d809-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="7d809-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7d809-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7d809-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7d809-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





