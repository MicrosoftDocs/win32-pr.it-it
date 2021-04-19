---
title: Controls. playItem, metodo
description: Il metodo playItem riproduce l'elemento multimediale specificato. | Controls. playItem, metodo
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- Metodo playItem Windows Media Player
- Metodo playItem Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331866"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="9ef29-107">Controls. playItem, metodo</span><span class="sxs-lookup"><span data-stu-id="9ef29-107">Controls.playItem method</span></span>

<span data-ttu-id="9ef29-108">Il metodo **playItem** riproduce l'elemento multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="9ef29-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef29-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ef29-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="9ef29-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ef29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef29-111">*theMediaItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ef29-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ef29-112">Oggetto **multimediale** da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="9ef29-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef29-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ef29-113">Return value</span></span>

<span data-ttu-id="9ef29-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9ef29-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef29-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ef29-115">Remarks</span></span>

<span data-ttu-id="9ef29-116">L'elemento multimediale verrà caricato e riprodotto automaticamente, indipendentemente dal valore delle *Impostazioni*. Proprietà di **avvio automatico** .</span><span class="sxs-lookup"><span data-stu-id="9ef29-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="9ef29-117">Per caricare un elemento senza riprodurlo automaticamente, impostare *le impostazioni*. **avvio automatico** a false e assegnazione di un valore al *lettore*. **URL**, dopo il quale è possibile chiamare **Play** per iniziare a riprodurre l'elemento.</span><span class="sxs-lookup"><span data-stu-id="9ef29-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="9ef29-118">Nota</span><span class="sxs-lookup"><span data-stu-id="9ef29-118">Note</span></span>

<span data-ttu-id="9ef29-119">**playItem** funziona solo con gli elementi in *currentPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="9ef29-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="9ef29-120">La chiamata di **playItem** con un riferimento a un elemento multimediale salvato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9ef29-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="9ef29-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="9ef29-121">Examples</span></span>

<span data-ttu-id="9ef29-122">Nell'esempio JScript seguente viene usato **playItem** per riprodurre un elemento multimediale dalla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="9ef29-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="9ef29-123">L'elemento da riprodurre viene scelto in base alla relativa posizione nella playlist.</span><span class="sxs-lookup"><span data-stu-id="9ef29-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="9ef29-124">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9ef29-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="9ef29-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ef29-125">Requirements</span></span>



| <span data-ttu-id="9ef29-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef29-126">Requirement</span></span> | <span data-ttu-id="9ef29-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9ef29-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef29-128">Versione</span><span class="sxs-lookup"><span data-stu-id="9ef29-128">Version</span></span><br/> | <span data-ttu-id="9ef29-129">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="9ef29-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9ef29-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9ef29-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ef29-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ef29-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef29-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ef29-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef29-133">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="9ef29-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="9ef29-134">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="9ef29-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





