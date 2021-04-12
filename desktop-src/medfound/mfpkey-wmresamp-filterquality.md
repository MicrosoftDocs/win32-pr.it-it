---
description: Specifica la qualità dell'output.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: Proprietà MFPKEY_WMRESAMP_FILTERQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226535"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a><span data-ttu-id="051a3-103">MFPKEY \_ WMRESAMP- \_ Proprietà FILTERQUALITY</span><span class="sxs-lookup"><span data-stu-id="051a3-103">MFPKEY\_WMRESAMP\_FILTERQUALITY Property</span></span>

<span data-ttu-id="051a3-104">Specifica la qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="051a3-104">Specifies the quality of the output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="051a3-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="051a3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="051a3-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="051a3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="051a3-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="051a3-107">Data Type</span></span>

<span data-ttu-id="051a3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="051a3-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="051a3-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="051a3-109">Applies To</span></span>

-   [<span data-ttu-id="051a3-110">DSP ricampionatore audio</span><span class="sxs-lookup"><span data-stu-id="051a3-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="051a3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="051a3-111">Remarks</span></span>

<span data-ttu-id="051a3-112">L'intervallo valido di questa proprietà è compreso tra 1 e 60, inclusi.</span><span class="sxs-lookup"><span data-stu-id="051a3-112">The valid range of this property is 1 to 60, inclusive.</span></span> <span data-ttu-id="051a3-113">I valori più elevati producono un output di qualità superiore, ma introducono maggiore latenza.</span><span class="sxs-lookup"><span data-stu-id="051a3-113">Higher values produce higher-quality output, but introduce more latency.</span></span> <span data-ttu-id="051a3-114">Il valore 1 è essenzialmente uguale all'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="051a3-114">A value of 1 is essentially the same as linear interpolation.</span></span>

## <a name="requirements"></a><span data-ttu-id="051a3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="051a3-115">Requirements</span></span>



| <span data-ttu-id="051a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="051a3-116">Requirement</span></span> | <span data-ttu-id="051a3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="051a3-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="051a3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="051a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="051a3-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="051a3-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="051a3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="051a3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="051a3-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="051a3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="051a3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="051a3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="051a3-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="051a3-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="051a3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="051a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="051a3-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="051a3-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
