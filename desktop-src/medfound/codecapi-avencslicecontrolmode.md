---
description: Specifica la modalità di controllo sezionamento. I valori validi sono 0, 1 e 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Proprietà CODECAPI_AVEncSliceControlMode (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966407"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="6d8d5-104">Proprietà AVEncSliceControlMode di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="6d8d5-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="6d8d5-105">Specifica la modalità di controllo sezionamento.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-105">Specifies the slice control mode.</span></span> <span data-ttu-id="6d8d5-106">I valori validi sono 0, 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="6d8d5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6d8d5-107">Data type</span></span>

<span data-ttu-id="6d8d5-108">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="6d8d5-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6d8d5-109">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="6d8d5-109">Property GUID</span></span>

<span data-ttu-id="6d8d5-110">**Codecapis \_ AVEncSliceControlMode**</span><span class="sxs-lookup"><span data-stu-id="6d8d5-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="6d8d5-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6d8d5-111">Property value</span></span>

<span data-ttu-id="6d8d5-112">Valori della modalità di controllo Slice:</span><span class="sxs-lookup"><span data-stu-id="6d8d5-112">Slice control mode values:</span></span>



| <span data-ttu-id="6d8d5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6d8d5-113">Value</span></span>                                                                        | <span data-ttu-id="6d8d5-114">Significato</span><span class="sxs-lookup"><span data-stu-id="6d8d5-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d8d5-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d8d5-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6d8d5-116">L'impostazione di questo valore su 0 indica che la proprietà [ \_ AVEncSliceControlSize di codecapis](codecapi-avencslicecontrolsize.md) specificherà le dimensioni delle sezioni in unità di macroblocchi per sezione.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="6d8d5-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6d8d5-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6d8d5-118">Impostando questo valore su 1 si indica che la proprietà [ \_ AVEncSliceControlSize di codecapis](codecapi-avencslicecontrolsize.md) specificherà le dimensioni delle sezioni in unità di bit per sezione.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="6d8d5-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6d8d5-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6d8d5-120">Impostando questo valore su 2 si indica che la proprietà [ \_ AVEncSliceControlSize di codecapis](codecapi-avencslicecontrolsize.md) specificherà le dimensioni delle sezioni in unità di macroblocco righe per sezione.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="6d8d5-121">Il codificatore restituisce i valori supportati.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8d5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d8d5-122">Remarks</span></span>

<span data-ttu-id="6d8d5-123">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="6d8d5-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="6d8d5-124">È consigliabile che il codificatore supporti [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="6d8d5-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="6d8d5-125">Se [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) non viene chiamato per codecapis \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) per codecapis \_ AVENCSLICECONTROLMODE può restituire **VFW \_ E \_ codecapi \_ senza \_ \_ valore corrente**.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="6d8d5-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) può restituire **VFW \_ E \_ codecapi \_ non per \_ impostazione predefinita** per codecapis \_ AVEncSliceControlMode.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="6d8d5-127">Il valore predefinito consigliato è 2 (dimensione in MB di riga per sezione).</span><span class="sxs-lookup"><span data-stu-id="6d8d5-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="6d8d5-128">Si tratta di un'API statica, che significa che l'applicazione ha vinto la modifica quando il codificatore è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="6d8d5-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="6d8d5-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="6d8d5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d8d5-130">Requirements</span></span>



| <span data-ttu-id="6d8d5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8d5-131">Requirement</span></span> | <span data-ttu-id="6d8d5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6d8d5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8d5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d8d5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8d5-134">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6d8d5-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="6d8d5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d8d5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8d5-136">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6d8d5-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6d8d5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d8d5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d8d5-138"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d8d5-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d8d5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d8d5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8d5-140">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6d8d5-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

