---
description: Specifica se il DSP di acquisizione vocale archivia le statistiche relative al timestamp nel registro di sistema.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Proprietà MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309115"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="f39ef-103">MFPKEY \_ WMAAECMA \_ - \_ recupero \_ proprietà statistiche Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="f39ef-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="f39ef-104">Specifica se il DSP di acquisizione vocale archivia le statistiche relative al timestamp nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f39ef-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f39ef-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f39ef-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f39ef-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f39ef-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f39ef-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f39ef-107">Data Type</span></span>

<span data-ttu-id="f39ef-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="f39ef-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="f39ef-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="f39ef-109">Default Value</span></span>

<span data-ttu-id="f39ef-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="f39ef-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="f39ef-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="f39ef-111">Applies To</span></span>

-   [<span data-ttu-id="f39ef-112">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="f39ef-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="f39ef-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f39ef-113">Remarks</span></span>

<span data-ttu-id="f39ef-114">Gli algoritmi AEC (Acoustic Echo Cancel) dipendono da timestamp accurati nei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="f39ef-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="f39ef-115">In realtà, i timestamp sono spesso imperfetti e diversi dispositivi audio possono presentare frequenze diverse di varianza e tendenza.</span><span class="sxs-lookup"><span data-stu-id="f39ef-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="f39ef-116">Quando AEC è abilitato, il DSP raccoglie le statistiche relative ai timestamp e usa queste informazioni per compensare le imprecisioni.</span><span class="sxs-lookup"><span data-stu-id="f39ef-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="f39ef-117">Se il valore di questa proprietà è VARIANT \_ true, il DSP Salva le statistiche che raccoglie nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f39ef-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="f39ef-118">La volta successiva che il DSP esegue l'AEC usando la stessa coppia di dispositivi audio, legge le informazioni statistiche dal registro di sistema, consentendo al DSP di eseguire in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="f39ef-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="f39ef-119">Se si imposta il valore di questa proprietà su VARIANT \_ true e si usa il DSP in modalità filtro, è necessario impostare anche la proprietà [ \_ \_ \_ GUID MFPKEY WMAAECMA DEVICEPAIR](mfpkey-wmaaecma-devicepair-guidproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f39ef-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="f39ef-120">In modalità origine questa operazione non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="f39ef-120">In source mode, this is not required.</span></span>

<span data-ttu-id="f39ef-121">Il valore predefinito di questa proprietà è VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="f39ef-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="f39ef-122">Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.</span><span class="sxs-lookup"><span data-stu-id="f39ef-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f39ef-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f39ef-123">Requirements</span></span>



| <span data-ttu-id="f39ef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f39ef-124">Requirement</span></span> | <span data-ttu-id="f39ef-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f39ef-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f39ef-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f39ef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f39ef-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f39ef-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f39ef-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f39ef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f39ef-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f39ef-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f39ef-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f39ef-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f39ef-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f39ef-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f39ef-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f39ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39ef-133">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f39ef-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f39ef-134">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="f39ef-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
