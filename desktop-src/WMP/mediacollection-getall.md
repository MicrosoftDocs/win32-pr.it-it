---
title: Mediacollection. getAll, metodo
description: Il metodo getAll recupera una playlist contenente tutti gli elementi multimediali nella libreria.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- Metodo getAll Windows Media Player
- Metodo getAll Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getAll
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330355"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="bada2-106">Mediacollection. getAll, metodo</span><span class="sxs-lookup"><span data-stu-id="bada2-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="bada2-107">Il metodo **GetAll** recupera una playlist contenente tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="bada2-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="bada2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bada2-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="bada2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bada2-109">Parameters</span></span>

<span data-ttu-id="bada2-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bada2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bada2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bada2-111">Return value</span></span>

<span data-ttu-id="bada2-112">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="bada2-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bada2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bada2-113">Remarks</span></span>

<span data-ttu-id="bada2-114">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="bada2-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="bada2-115">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bada2-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bada2-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="bada2-116">Examples</span></span>

<span data-ttu-id="bada2-117">Nell'esempio JScript seguente viene utilizzato *mediacollection*. **GetAll** per riprodurre elementi multimediali in modo casuale dalla raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="bada2-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="bada2-118">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="bada2-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="bada2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bada2-119">Requirements</span></span>



| <span data-ttu-id="bada2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bada2-120">Requirement</span></span> | <span data-ttu-id="bada2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bada2-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bada2-122">Versione</span><span class="sxs-lookup"><span data-stu-id="bada2-122">Version</span></span><br/> | <span data-ttu-id="bada2-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="bada2-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bada2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bada2-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bada2-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bada2-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bada2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bada2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bada2-127">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="bada2-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="bada2-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="bada2-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="bada2-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bada2-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bada2-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bada2-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





