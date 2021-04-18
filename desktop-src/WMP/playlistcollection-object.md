---
title: PlaylistCollection (oggetto)
description: L'oggetto playlistCollection fornisce un modo per organizzare le playlist.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Finestra di Media Player oggetto PlaylistCollection
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299057"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="39c88-104">PlaylistCollection (oggetto)</span><span class="sxs-lookup"><span data-stu-id="39c88-104">PlaylistCollection Object</span></span>

<span data-ttu-id="39c88-105">L'oggetto **PlaylistCollection** fornisce un modo per organizzare le playlist.</span><span class="sxs-lookup"><span data-stu-id="39c88-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="39c88-106">L'oggetto **PlaylistCollection** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="39c88-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="39c88-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="39c88-107">Method</span></span>                                                  | <span data-ttu-id="39c88-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39c88-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39c88-109">getAll</span><span class="sxs-lookup"><span data-stu-id="39c88-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="39c88-110">Recupera un oggetto [PlaylistArray](playlistarray-object.md) contenente tutte le playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="39c88-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="39c88-111">getByName</span><span class="sxs-lookup"><span data-stu-id="39c88-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="39c88-112">Recupera un oggetto [PlaylistArray](playlistarray-object.md) contenente le playlist con il nome specificato, se esistente.</span><span class="sxs-lookup"><span data-stu-id="39c88-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="39c88-113">importPlaylist</span><span class="sxs-lookup"><span data-stu-id="39c88-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="39c88-114">Aggiunge una playlist statica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="39c88-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="39c88-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="39c88-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="39c88-116">Recupera un valore che indica se la playlist specificata si trova nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="39c88-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| [<span data-ttu-id="39c88-117">Nuova playlist</span><span class="sxs-lookup"><span data-stu-id="39c88-117">newPlaylist</span></span>](playlistcollection-newplaylist.md)       | <span data-ttu-id="39c88-118">Crea una nuova playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="39c88-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="39c88-119">remove</span><span class="sxs-lookup"><span data-stu-id="39c88-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="39c88-120">Rimuove una playlist dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="39c88-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="39c88-121">Eliminata</span><span class="sxs-lookup"><span data-stu-id="39c88-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="39c88-122">Sposta una playlist nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="39c88-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="39c88-123">È possibile accedere all'oggetto **PlaylistCollection** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="39c88-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="39c88-124">Oggetto</span><span class="sxs-lookup"><span data-stu-id="39c88-124">Object</span></span>                      | <span data-ttu-id="39c88-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39c88-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="39c88-126">Player</span><span class="sxs-lookup"><span data-stu-id="39c88-126">Player</span></span>](player-object.md) | [<span data-ttu-id="39c88-127">playlistCollection</span><span class="sxs-lookup"><span data-stu-id="39c88-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="39c88-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c88-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c88-129">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="39c88-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




