---
description: Rappresenta il tipo di origine del frame.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Attributo MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309574"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a><span data-ttu-id="9c70e-103">\_Attributo di \_ \_ tipi origine frame dell'attributo MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="9c70e-103">MF\_DEVICESTREAM\_ATTRIBUTE\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="9c70e-104">Rappresenta il tipo di origine del frame.</span><span class="sxs-lookup"><span data-stu-id="9c70e-104">Represents the frame source type.</span></span>

## <a name="data-type"></a><span data-ttu-id="9c70e-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9c70e-105">Data type</span></span>

<span data-ttu-id="9c70e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9c70e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c70e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c70e-107">Remarks</span></span>

<span data-ttu-id="9c70e-108">Questo valore di questo attributo deve essere una maschera di maschera di uno o più valori dell'enumerazione [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) .</span><span class="sxs-lookup"><span data-stu-id="9c70e-108">This value of this attribute should be a bitmask of one or more values from the [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) enumeration.</span></span> <span data-ttu-id="9c70e-109">Per supportare la compatibilità con le versioni precedenti, quando questo attributo non è definito per un tipo di supporto, si presuppone che il valore di **MFFrameSourceTypes:: color**.</span><span class="sxs-lookup"><span data-stu-id="9c70e-109">To support backward compatibility, when this attribute is not defined for a media type, it is assumed to have the value **MFFrameSourceTypes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c70e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c70e-110">Requirements</span></span>



| <span data-ttu-id="9c70e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c70e-111">Requirement</span></span> | <span data-ttu-id="9c70e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9c70e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c70e-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c70e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9c70e-114">Solo app desktop Windows 10 versione 1607 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c70e-114">Windows 10, version 1607 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9c70e-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c70e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9c70e-116">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="9c70e-116">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c70e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c70e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c70e-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c70e-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




