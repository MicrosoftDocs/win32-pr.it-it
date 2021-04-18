---
title: PlaylistCollection. Metodo eliminato
description: Il metodo IsValid recupera un valore che indica se la playlist specificata si trova nella cartella Deleted Items.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- Metodo eliminato Media Player Windows
- Metodo di eliminazione di Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo eliminato
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329429"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="6ac3b-106">PlaylistCollection. Metodo eliminato</span><span class="sxs-lookup"><span data-stu-id="6ac3b-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="6ac3b-107">Il **Metodo IsValid** recupera un valore che indica se la playlist specificata si trova nella cartella Deleted Items.</span><span class="sxs-lookup"><span data-stu-id="6ac3b-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac3b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ac3b-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="6ac3b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ac3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac3b-110">*playlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ac3b-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac3b-111">Oggetto **playlist** da cercare.</span><span class="sxs-lookup"><span data-stu-id="6ac3b-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac3b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ac3b-112">Return value</span></span>

<span data-ttu-id="6ac3b-113">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="6ac3b-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="6ac3b-114">**Windows Media Player 10 Mobile**: questo metodo restituisce sempre **false**.</span><span class="sxs-lookup"><span data-stu-id="6ac3b-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac3b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ac3b-115">Requirements</span></span>



| <span data-ttu-id="6ac3b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac3b-116">Requirement</span></span> | <span data-ttu-id="6ac3b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6ac3b-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac3b-118">Versione</span><span class="sxs-lookup"><span data-stu-id="6ac3b-118">Version</span></span><br/> | <span data-ttu-id="6ac3b-119">Windows Media Player versione 7,0, Windows Media Player versione 7,1 o Windows Media Player per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ac3b-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="6ac3b-120">Questo metodo non è supportato per Windows Media Player 9 Series o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6ac3b-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="6ac3b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6ac3b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ac3b-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ac3b-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="6ac3b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ac3b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac3b-124">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="6ac3b-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





