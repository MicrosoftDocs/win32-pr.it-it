---
description: Specifica il tipo di unità contenuta in un IMFSample in una \_ raccolta ForwardedDecodeUnits MFSampleExtension.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Enumerazione MF_CUSTOM_DECODE_UNIT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226647"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="56bdb-103">\_Enumerazione del \_ tipo di \_ unità di decodifica personalizzato MF \_</span><span class="sxs-lookup"><span data-stu-id="56bdb-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="56bdb-104">Specifica il tipo di unità contenuta in un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in una raccolta [ \_ ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md) .</span><span class="sxs-lookup"><span data-stu-id="56bdb-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="56bdb-105">Membri</span><span class="sxs-lookup"><span data-stu-id="56bdb-105">Members</span></span>



| <span data-ttu-id="56bdb-106">Membro</span><span class="sxs-lookup"><span data-stu-id="56bdb-106">Member</span></span>                    | <span data-ttu-id="56bdb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56bdb-107">Description</span></span>                                                             | <span data-ttu-id="56bdb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="56bdb-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="56bdb-109">**MF \_ Decode \_ unit \_ NAL**</span><span class="sxs-lookup"><span data-stu-id="56bdb-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="56bdb-110">Il tipo di unità è NALU (Network Abstraction Layer Unit).</span><span class="sxs-lookup"><span data-stu-id="56bdb-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="56bdb-111">0</span><span class="sxs-lookup"><span data-stu-id="56bdb-111">0</span></span>     |
| <span data-ttu-id="56bdb-112">**MF \_ decodifica \_ unità \_ sei**</span><span class="sxs-lookup"><span data-stu-id="56bdb-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="56bdb-113">Il tipo di unità è informazioni aggiuntive sul miglioramento (SEI).</span><span class="sxs-lookup"><span data-stu-id="56bdb-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="56bdb-114">1</span><span class="sxs-lookup"><span data-stu-id="56bdb-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="56bdb-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="56bdb-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="56bdb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56bdb-116">Requirements</span></span>



| <span data-ttu-id="56bdb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="56bdb-117">Requirement</span></span> | <span data-ttu-id="56bdb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="56bdb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56bdb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56bdb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56bdb-120">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="56bdb-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="56bdb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56bdb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56bdb-122">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="56bdb-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="56bdb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56bdb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56bdb-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56bdb-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




