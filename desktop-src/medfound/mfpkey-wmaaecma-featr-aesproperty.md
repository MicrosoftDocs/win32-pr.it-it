---
description: Specifica il numero di volte in cui il DSP di acquisizione vocale esegue l'eliminazione dell'eco acustico (AES) sul segnale residuo.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Proprietà MFPKEY_WMAAECMA_FEATR_AES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309136"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="88fd2-103">\_ \_ Proprietà AES MFPKEY WMAAECMA featr \_</span><span class="sxs-lookup"><span data-stu-id="88fd2-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="88fd2-104">Specifica il numero di volte in cui il DSP di acquisizione vocale esegue l'eliminazione dell'eco acustico (AES) sul segnale residuo.</span><span class="sxs-lookup"><span data-stu-id="88fd2-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="88fd2-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="88fd2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="88fd2-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="88fd2-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="88fd2-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="88fd2-107">Data Type</span></span>

<span data-ttu-id="88fd2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="88fd2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="88fd2-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="88fd2-109">Default Value</span></span>

<span data-ttu-id="88fd2-110">0</span><span class="sxs-lookup"><span data-stu-id="88fd2-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="88fd2-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="88fd2-111">Applies To</span></span>

-   [<span data-ttu-id="88fd2-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="88fd2-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="88fd2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="88fd2-113">Remarks</span></span>

<span data-ttu-id="88fd2-114">Il DSP di acquisizione vocale può eseguire AES sul segnale residuo dopo l'annullamento di Echo.</span><span class="sxs-lookup"><span data-stu-id="88fd2-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="88fd2-115">Il valore di questa proprietà può essere 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="88fd2-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="88fd2-116">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="88fd2-116">The default value is 0.</span></span> <span data-ttu-id="88fd2-117">Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="88fd2-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="88fd2-118">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.</span><span class="sxs-lookup"><span data-stu-id="88fd2-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="88fd2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88fd2-119">Requirements</span></span>



| <span data-ttu-id="88fd2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="88fd2-120">Requirement</span></span> | <span data-ttu-id="88fd2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="88fd2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88fd2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88fd2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88fd2-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88fd2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="88fd2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88fd2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88fd2-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88fd2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88fd2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88fd2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88fd2-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88fd2-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88fd2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88fd2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88fd2-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88fd2-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="88fd2-130">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="88fd2-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
