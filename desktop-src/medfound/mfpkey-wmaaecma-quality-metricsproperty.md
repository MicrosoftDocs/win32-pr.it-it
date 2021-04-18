---
description: Recupera le metriche qualitative nell'annullamento dell'eco acustico (AEC) dal DSP di acquisizione voce.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: Proprietà MFPKEY_WMAAECMA_QUALITY_METRICS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309116"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="d248d-103">\_ \_ Proprietà metrica qualità MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="d248d-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="d248d-104">Recupera le metriche qualitative nell'annullamento dell'eco acustico (AEC) dal DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="d248d-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d248d-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d248d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d248d-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d248d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d248d-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d248d-107">Data Type</span></span>

<span data-ttu-id="d248d-108">\_BLOB VT</span><span class="sxs-lookup"><span data-stu-id="d248d-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="d248d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d248d-109">Remarks</span></span>

<span data-ttu-id="d248d-110">Il valore di questa proprietà è una struttura dello [ \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) .</span><span class="sxs-lookup"><span data-stu-id="d248d-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="d248d-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d248d-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="d248d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d248d-112">Requirements</span></span>



| <span data-ttu-id="d248d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d248d-113">Requirement</span></span> | <span data-ttu-id="d248d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d248d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d248d-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d248d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d248d-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d248d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d248d-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d248d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d248d-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d248d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d248d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d248d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d248d-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d248d-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d248d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d248d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d248d-122">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d248d-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d248d-123">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="d248d-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
