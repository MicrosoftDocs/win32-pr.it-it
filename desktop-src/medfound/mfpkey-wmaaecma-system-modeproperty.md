---
description: Imposta la modalità di elaborazione per il DSP di acquisizione voce.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Proprietà MFPKEY_WMAAECMA_SYSTEM_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310265"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="7ceb1-103">\_ \_ Proprietà modalità di sistema WMAAECMA di MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="7ceb1-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="7ceb1-104">Imposta la modalità di elaborazione per il DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="7ceb1-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7ceb1-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7ceb1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7ceb1-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7ceb1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7ceb1-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7ceb1-107">Data Type</span></span>

<span data-ttu-id="7ceb1-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7ceb1-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="7ceb1-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="7ceb1-109">Applies To</span></span>

-   [<span data-ttu-id="7ceb1-110">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="7ceb1-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="7ceb1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ceb1-111">Remarks</span></span>

<span data-ttu-id="7ceb1-112">Il valore di questa proprietà è un membro dell'enumerazione [della \_ \_ modalità di sistema AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .</span><span class="sxs-lookup"><span data-stu-id="7ceb1-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="7ceb1-113">La proprietà deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ceb1-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="7ceb1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7ceb1-114">Value</span></span> | <span data-ttu-id="7ceb1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ceb1-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="7ceb1-116">0</span><span class="sxs-lookup"><span data-stu-id="7ceb1-116">0</span></span>     | <span data-ttu-id="7ceb1-117">Modalità di annullamento audio Echo (AEC)</span><span class="sxs-lookup"><span data-stu-id="7ceb1-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="7ceb1-118">2</span><span class="sxs-lookup"><span data-stu-id="7ceb1-118">2</span></span>     | <span data-ttu-id="7ceb1-119">Modalità solo elaborazione array Microfoni (mappa)</span><span class="sxs-lookup"><span data-stu-id="7ceb1-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="7ceb1-120">4</span><span class="sxs-lookup"><span data-stu-id="7ceb1-120">4</span></span>     | <span data-ttu-id="7ceb1-121">Modalità AEC e MAP</span><span class="sxs-lookup"><span data-stu-id="7ceb1-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="7ceb1-122">5</span><span class="sxs-lookup"><span data-stu-id="7ceb1-122">5</span></span>     | <span data-ttu-id="7ceb1-123">Modalità AEC o MAP</span><span class="sxs-lookup"><span data-stu-id="7ceb1-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="7ceb1-124">È necessario impostare questa proprietà prima di usare il DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="7ceb1-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="7ceb1-125">Dopo aver impostato questa proprietà, è possibile usare il DSP con le impostazioni predefinite o impostare proprietà aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="7ceb1-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ceb1-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ceb1-126">Requirements</span></span>



| <span data-ttu-id="7ceb1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ceb1-127">Requirement</span></span> | <span data-ttu-id="7ceb1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7ceb1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ceb1-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ceb1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7ceb1-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ceb1-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7ceb1-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ceb1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7ceb1-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ceb1-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ceb1-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ceb1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ceb1-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb1-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ceb1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ceb1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ceb1-136">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ceb1-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7ceb1-137">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="7ceb1-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
