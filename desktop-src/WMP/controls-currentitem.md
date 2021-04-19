---
title: Controls. currentItem
description: La proprietà currentItem specifica o recupera l'elemento multimediale corrente.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Media Player di Windows Controls. currentItem
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330123"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="9f509-104">Controls. currentItem</span><span class="sxs-lookup"><span data-stu-id="9f509-104">Controls.currentItem</span></span>

<span data-ttu-id="9f509-105">La proprietà **CurrentItem** specifica o recupera l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="9f509-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="9f509-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9f509-106">Possible Values</span></span>

<span data-ttu-id="9f509-107">Questa proprietà è un oggetto **multimediale** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9f509-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f509-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f509-108">Remarks</span></span>

<span data-ttu-id="9f509-109">Questo metodo funziona solo con gli elementi in *Player*. **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="9f509-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="9f509-110">La chiamata di **CurrentItem** con un riferimento a un elemento multimediale salvato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9f509-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="9f509-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="9f509-111">Examples</span></span>

<span data-ttu-id="9f509-112">Nell'esempio di codice JScript seguente viene usato **CurrentItem** per impostare l'elemento multimediale corrente del controllo del lettore sul valore selezionato in un elemento HTML SELECT.</span><span class="sxs-lookup"><span data-stu-id="9f509-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="9f509-113">La playlist corrente è stata specificata per la prima volta tramite *PlaylistCollection*. **GetByName**.</span><span class="sxs-lookup"><span data-stu-id="9f509-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="9f509-114">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9f509-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="9f509-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f509-115">Requirements</span></span>



| <span data-ttu-id="9f509-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f509-116">Requirement</span></span> | <span data-ttu-id="9f509-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9f509-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f509-118">Versione</span><span class="sxs-lookup"><span data-stu-id="9f509-118">Version</span></span><br/> | <span data-ttu-id="9f509-119">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="9f509-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9f509-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9f509-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="9f509-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f509-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f509-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f509-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f509-123">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="9f509-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="9f509-124">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="9f509-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="9f509-125">**PlaylistCollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="9f509-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





