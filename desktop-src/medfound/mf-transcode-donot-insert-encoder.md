---
description: Specifica se un codificatore deve essere incluso nella topologia transcodifica.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Attributo MF_TRANSCODE_DONOT_INSERT_ENCODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308428"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a><span data-ttu-id="730af-103">\_ \_ \_ \_ Attributo encoder Insert encoder di MF transcode</span><span class="sxs-lookup"><span data-stu-id="730af-103">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER attribute</span></span>

<span data-ttu-id="730af-104">Specifica se un codificatore deve essere incluso nella topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="730af-104">Specifies whether an encoder must be included in the transcode topology.</span></span>

<span data-ttu-id="730af-105">La funzione [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) controlla questo attributo durante la compilazione della topologia.</span><span class="sxs-lookup"><span data-stu-id="730af-105">The [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function checks this attribute during topology building.</span></span> <span data-ttu-id="730af-106">Se questo attributo non è impostato, nella topologia transcodifica viene inserito un codificatore.</span><span class="sxs-lookup"><span data-stu-id="730af-106">If this attribute is not set, an encoder is inserted in the transcode topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="730af-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="730af-107">Data type</span></span>

<span data-ttu-id="730af-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="730af-108">**UINT32**</span></span>



| <span data-ttu-id="730af-109">Valore</span><span class="sxs-lookup"><span data-stu-id="730af-109">Value</span></span>                                                                        | <span data-ttu-id="730af-110">Significato</span><span class="sxs-lookup"><span data-stu-id="730af-110">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="730af-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="730af-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="730af-112">Viene inserito un codificatore nella topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="730af-112">An encoder is inserted in the transcode topology.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="730af-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="730af-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="730af-114">Un codificatore non è incluso nella topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="730af-114">An encoder is not included in the transcode topology.</span></span> <span data-ttu-id="730af-115">Il nodo di origine è connesso al nodo di output.</span><span class="sxs-lookup"><span data-stu-id="730af-115">The source node is connected to the output node.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="730af-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="730af-116">Remarks</span></span>

<span data-ttu-id="730af-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="730af-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="730af-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="730af-118">Requirements</span></span>



| <span data-ttu-id="730af-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="730af-119">Requirement</span></span> | <span data-ttu-id="730af-120">Valore</span><span class="sxs-lookup"><span data-stu-id="730af-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="730af-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="730af-121">Minimum supported client</span></span><br/> | <span data-ttu-id="730af-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="730af-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="730af-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="730af-123">Minimum supported server</span></span><br/> | <span data-ttu-id="730af-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="730af-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="730af-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="730af-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="730af-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="730af-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="730af-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="730af-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730af-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="730af-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="730af-129">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="730af-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




