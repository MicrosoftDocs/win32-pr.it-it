---
description: Specifica se il video H. 264 remux MFT dovrebbe contrassegnare le immagini come punto di pulitura per una migliore capacità di ricerca. Questo può causare danneggiamenti nelle ricerche in file MP4 finali non conformi.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Attributo MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310210"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="5fec6-104">\_ \_ Immagine di REMUX di MFT contrassegnata \_ \_ \_ come \_ \_ attributo punto di pulizia</span><span class="sxs-lookup"><span data-stu-id="5fec6-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="5fec6-105">Specifica se il video H. 264 remux MFT dovrebbe contrassegnare le immagini come punto di pulitura per una migliore capacità di ricerca.</span><span class="sxs-lookup"><span data-stu-id="5fec6-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="5fec6-106">Questo può causare danneggiamenti nelle ricerche in file MP4 finali non conformi.</span><span class="sxs-lookup"><span data-stu-id="5fec6-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="5fec6-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5fec6-107">Data type</span></span>

<span data-ttu-id="5fec6-108">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fec6-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5fec6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fec6-109">Remarks</span></span>

<span data-ttu-id="5fec6-110">L'immagine del punto di pulizia deve essere compressa IDR immagini per definizione.</span><span class="sxs-lookup"><span data-stu-id="5fec6-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="5fec6-111">Questa operazione non è consigliata per la registrazione o la remuxing di file MP4, a meno che tale esercizio non produca alcuni file pseudo-MP4 intermedi per la modifica dei video.</span><span class="sxs-lookup"><span data-stu-id="5fec6-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fec6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fec6-112">Requirements</span></span>



| <span data-ttu-id="5fec6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fec6-113">Requirement</span></span> | <span data-ttu-id="5fec6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5fec6-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fec6-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fec6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5fec6-116">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5fec6-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5fec6-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fec6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5fec6-118">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5fec6-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="5fec6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fec6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fec6-120"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fec6-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="5fec6-121">IDL</span><span class="sxs-lookup"><span data-stu-id="5fec6-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5fec6-122"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5fec6-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fec6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fec6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fec6-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fec6-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




