---
title: PLAYLIST. dropDownList
description: L'attributo dropDownList specifica o recupera un valore che indica quali elementi vengono visualizzati nella casella di riepilogo a discesa per una determinata istanza dell'elemento PLAYLIST.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- PLAYLIST. dropDownList Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326106"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="0720b-104">PLAYLIST. dropDownList</span><span class="sxs-lookup"><span data-stu-id="0720b-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="0720b-105">L'attributo **dropDownList** specifica o recupera un valore che indica quali elementi vengono visualizzati nella casella di riepilogo a discesa per una determinata istanza dell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="0720b-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="0720b-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0720b-106">Possible Values</span></span>

<span data-ttu-id="0720b-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0720b-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="0720b-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0720b-108">Value</span></span>       | <span data-ttu-id="0720b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0720b-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0720b-110">showAlbums</span><span class="sxs-lookup"><span data-stu-id="0720b-110">showAlbums</span></span>  | <span data-ttu-id="0720b-111">Mostra gli album.</span><span class="sxs-lookup"><span data-stu-id="0720b-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="0720b-112">showAll</span><span class="sxs-lookup"><span data-stu-id="0720b-112">showAll</span></span>     | <span data-ttu-id="0720b-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0720b-113">Default.</span></span> <span data-ttu-id="0720b-114">Mostra tutti gli elementi disponibili, incluse le playlist CD, le playlist utente e i set di impostazioni radio.</span><span class="sxs-lookup"><span data-stu-id="0720b-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="0720b-115">showCD</span><span class="sxs-lookup"><span data-stu-id="0720b-115">showCD</span></span>      | <span data-ttu-id="0720b-116">Mostra la playlist del CD.</span><span class="sxs-lookup"><span data-stu-id="0720b-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="0720b-117">showClips</span><span class="sxs-lookup"><span data-stu-id="0720b-117">showClips</span></span>   | <span data-ttu-id="0720b-118">Mostra tutte le clip.</span><span class="sxs-lookup"><span data-stu-id="0720b-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="0720b-119">showCurrent</span><span class="sxs-lookup"><span data-stu-id="0720b-119">showCurrent</span></span> | <span data-ttu-id="0720b-120">Mostra la playlist non salvata corrente.</span><span class="sxs-lookup"><span data-stu-id="0720b-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="0720b-121">showLibrary</span><span class="sxs-lookup"><span data-stu-id="0720b-121">showLibrary</span></span> | <span data-ttu-id="0720b-122">Mostra solo le playlist della libreria.</span><span class="sxs-lookup"><span data-stu-id="0720b-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="0720b-123">showRadio</span><span class="sxs-lookup"><span data-stu-id="0720b-123">showRadio</span></span>   | <span data-ttu-id="0720b-124">Mostra i set di impostazioni radio.</span><span class="sxs-lookup"><span data-stu-id="0720b-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="0720b-125">showQueries</span><span class="sxs-lookup"><span data-stu-id="0720b-125">showQueries</span></span> | <span data-ttu-id="0720b-126">Mostra le query.</span><span class="sxs-lookup"><span data-stu-id="0720b-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="0720b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0720b-127">Requirements</span></span>



| <span data-ttu-id="0720b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0720b-128">Requirement</span></span> | <span data-ttu-id="0720b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0720b-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0720b-130">Versione</span><span class="sxs-lookup"><span data-stu-id="0720b-130">Version</span></span><br/> | <span data-ttu-id="0720b-131">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="0720b-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0720b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0720b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0720b-133">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="0720b-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





