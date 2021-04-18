---
title: Player. currentPlaylist
description: La proprietà currentPlaylist specifica o recupera l'oggetto playlist corrente.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player. currentPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331223"
---
# <a name="playercurrentplaylist"></a><span data-ttu-id="6da97-104">Player. currentPlaylist</span><span class="sxs-lookup"><span data-stu-id="6da97-104">Player.currentPlaylist</span></span>

<span data-ttu-id="6da97-105">La proprietà currentPlaylist specifica o recupera l'oggetto **playlist** corrente.</span><span class="sxs-lookup"><span data-stu-id="6da97-105">The currentPlaylist property specifies or retrieves the current **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da97-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6da97-106">Syntax</span></span>

<span data-ttu-id="6da97-107">*Player* . **currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="6da97-107">*player* .**currentPlaylist**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6da97-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6da97-108">Possible Values</span></span>

<span data-ttu-id="6da97-109">Questa proprietà è un oggetto **playlist** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6da97-109">This property is a read/write **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6da97-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6da97-110">Remarks</span></span>

<span data-ttu-id="6da97-111">Se le *Impostazioni*. la proprietà **autostart** è true, la riproduzione viene avviata automaticamente quando si imposta **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="6da97-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="6da97-112">Questa proprietà accetta un oggetto playlist, che può essere acquisito in diversi modi, ad esempio chiamando *PlaylistArray*. **Item** o *PlaylistCollection*. **nuova playlist**.</span><span class="sxs-lookup"><span data-stu-id="6da97-112">This property takes a Playlist object, which can be acquired in several ways, such as by calling *PlaylistArray*.**item** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="6da97-113">Per caricare un elemento della **playlist** usando un nome file, impostare la proprietà URL o usare *Player*. **nuova playlist**.</span><span class="sxs-lookup"><span data-stu-id="6da97-113">To load a **Playlist** item using a file name, set the URL property or use *Player*.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="6da97-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="6da97-114">Examples</span></span>

<span data-ttu-id="6da97-115">Nell'esempio JScript seguente viene recuperata la prima playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="6da97-115">The following JScript example retrieves the first playlist in the library.</span></span> <span data-ttu-id="6da97-116">USA quindi **currentPlaylist** per fare in modo che la playlist recuperata sia la playlist corrente e quindi per visualizzare il nome della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="6da97-116">It then uses **currentPlaylist** to make the retrieved playlist the current playlist, and then to display the name of the current playlist.</span></span> <span data-ttu-id="6da97-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6da97-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a><span data-ttu-id="6da97-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6da97-118">Requirements</span></span>



| <span data-ttu-id="6da97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da97-119">Requirement</span></span> | <span data-ttu-id="6da97-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6da97-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6da97-121">Versione</span><span class="sxs-lookup"><span data-stu-id="6da97-121">Version</span></span><br/> | <span data-ttu-id="6da97-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6da97-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6da97-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6da97-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6da97-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da97-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da97-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6da97-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da97-126">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="6da97-126">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="6da97-127">**Player. nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="6da97-127">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="6da97-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="6da97-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="6da97-129">**PlaylistArray. Item**</span><span class="sxs-lookup"><span data-stu-id="6da97-129">**PlaylistArray.item**</span></span>](playlistarray-item.md)
</dt> <dt>

[<span data-ttu-id="6da97-130">**PlaylistCollection. nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="6da97-130">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="6da97-131">**Impostazioni. avvio automatico**</span><span class="sxs-lookup"><span data-stu-id="6da97-131">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





