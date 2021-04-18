---
description: Specifica se l'acquisizione voce DSP applica la delimitazione del guadagno del microfono.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Proprietà MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309119"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="590b5-103">\_Proprietà del \_ \_ limite Gain \_ MFPKEY WMAAECMA MIC</span><span class="sxs-lookup"><span data-stu-id="590b5-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="590b5-104">Specifica se l'acquisizione voce DSP applica la delimitazione del guadagno del microfono.</span><span class="sxs-lookup"><span data-stu-id="590b5-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="590b5-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="590b5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="590b5-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="590b5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="590b5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="590b5-107">Data Type</span></span>

<span data-ttu-id="590b5-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="590b5-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="590b5-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="590b5-109">Default Value</span></span>

<span data-ttu-id="590b5-110">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="590b5-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="590b5-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="590b5-111">Applies To</span></span>

-   [<span data-ttu-id="590b5-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="590b5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="590b5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="590b5-113">Remarks</span></span>

<span data-ttu-id="590b5-114">La limitazione del guadagno del microfono garantisce che il livello di guadagno del microfono sia corretto.</span><span class="sxs-lookup"><span data-stu-id="590b5-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="590b5-115">Se il guadagno è troppo elevato, il segnale acquisito potrebbe essere saturo e verrà ritagliato.</span><span class="sxs-lookup"><span data-stu-id="590b5-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="590b5-116">Il ritaglio è un effetto non lineare, che causerà un errore dell'algoritmo di annullamento dell'eco acustico (AEC).</span><span class="sxs-lookup"><span data-stu-id="590b5-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="590b5-117">Se il guadagno è troppo basso, il rapporto segnale/rumore è basso, che può anche causare un errore dell'algoritmo AEC o non funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="590b5-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="590b5-118">Questa proprietà può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="590b5-118">This property can have the following values.</span></span>



| <span data-ttu-id="590b5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="590b5-119">Value</span></span>          | <span data-ttu-id="590b5-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="590b5-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="590b5-121">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="590b5-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="590b5-122">Abilita delimitazione del guadagno del microfono.</span><span class="sxs-lookup"><span data-stu-id="590b5-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="590b5-123">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="590b5-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="590b5-124">Disabilitare la delimitazione del guadagno del microfono.</span><span class="sxs-lookup"><span data-stu-id="590b5-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="590b5-125">Il valore predefinito di questa proprietà è VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="590b5-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="590b5-126">La limitazione del guadagno del microfono si applica solo quando il DSP funziona in modalità origine.</span><span class="sxs-lookup"><span data-stu-id="590b5-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="590b5-127">In modalità filtro, l'applicazione deve verificare che il livello di guadagno del microfono sia corretto.</span><span class="sxs-lookup"><span data-stu-id="590b5-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="590b5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="590b5-128">Requirements</span></span>



| <span data-ttu-id="590b5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="590b5-129">Requirement</span></span> | <span data-ttu-id="590b5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="590b5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="590b5-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="590b5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="590b5-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="590b5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="590b5-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="590b5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="590b5-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="590b5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="590b5-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="590b5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="590b5-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="590b5-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="590b5-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="590b5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="590b5-138">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="590b5-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="590b5-139">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="590b5-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
