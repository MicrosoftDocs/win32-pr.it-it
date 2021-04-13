---
title: Oggetto MetadataPicture
description: L'oggetto MetadataPicture fornisce un modo per recuperare i valori dell'attributo di metadati WM/Picture. Questo attributo corrisponde agli album Art contenuti in un file multimediale digitale, non all'Art album scaricato tramite Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Media Player di Windows oggetto MetadataPicture
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473934"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="a62d3-105">Oggetto MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="a62d3-105">MetadataPicture Object</span></span>

<span data-ttu-id="a62d3-106">L'oggetto **MetadataPicture** fornisce un modo per recuperare i valori dell'attributo di metadati [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) .</span><span class="sxs-lookup"><span data-stu-id="a62d3-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="a62d3-107">Questo attributo corrisponde agli album Art contenuti in un file multimediale digitale, non all'Art album scaricato tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="a62d3-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="a62d3-108">L'oggetto **MetadataPicture** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="a62d3-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="a62d3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a62d3-109">Property</span></span>                                           | <span data-ttu-id="a62d3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a62d3-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="a62d3-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a62d3-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="a62d3-112">Recupera una descrizione dell'immagine dei metadati.</span><span class="sxs-lookup"><span data-stu-id="a62d3-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="a62d3-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="a62d3-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="a62d3-114">Recupera il tipo MIME dell'immagine dei metadati.</span><span class="sxs-lookup"><span data-stu-id="a62d3-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="a62d3-115">**pictureType**</span><span class="sxs-lookup"><span data-stu-id="a62d3-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="a62d3-116">Recupera il tipo di immagine dell'immagine dei metadati.</span><span class="sxs-lookup"><span data-stu-id="a62d3-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="a62d3-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="a62d3-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="a62d3-118">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="a62d3-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="a62d3-119">È possibile accedere all'oggetto **MetadataPicture** tramite il metodo seguente.</span><span class="sxs-lookup"><span data-stu-id="a62d3-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="a62d3-120">Oggetto</span><span class="sxs-lookup"><span data-stu-id="a62d3-120">Object</span></span>                        | <span data-ttu-id="a62d3-121">Metodo</span><span class="sxs-lookup"><span data-stu-id="a62d3-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="a62d3-122">**File multimediali**</span><span class="sxs-lookup"><span data-stu-id="a62d3-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="a62d3-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="a62d3-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="a62d3-124">Ai fini dell'illustrazione, `player.currentMedia.getItemInfoByType(name, language, index)` viene usato nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a62d3-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="a62d3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a62d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62d3-126">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="a62d3-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 