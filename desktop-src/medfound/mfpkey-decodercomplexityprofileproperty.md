---
description: Specifica il profilo di complessità del contenuto codificato.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Proprietà MFPKEY_DECODERCOMPLEXITYPROFILE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880818"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="db52b-103">\_Proprietà DECODERCOMPLEXITYPROFILE di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="db52b-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="db52b-104">Specifica il profilo di complessità del contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="db52b-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="db52b-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="db52b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="db52b-106">g \_ wszWMVCDecoderComplexityProfile</span><span class="sxs-lookup"><span data-stu-id="db52b-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="db52b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="db52b-107">Data Type</span></span>

<span data-ttu-id="db52b-108">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="db52b-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="db52b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="db52b-109">Remarks</span></span>

<span data-ttu-id="db52b-110">È possibile leggere questo valore solo dopo il completamento della codifica.</span><span class="sxs-lookup"><span data-stu-id="db52b-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="db52b-111">Per l'audio, questa proprietà ha uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="db52b-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="db52b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="db52b-112">Value</span></span> | <span data-ttu-id="db52b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db52b-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db52b-114">L1</span><span class="sxs-lookup"><span data-stu-id="db52b-114">"L1"</span></span>  | <span data-ttu-id="db52b-115">Codifica standard con frequenza di campionamento pari a 44,1 KHz e velocità in bit massima di 161 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="db52b-116">L2</span><span class="sxs-lookup"><span data-stu-id="db52b-116">"L2"</span></span>  | <span data-ttu-id="db52b-117">Codifica standard con frequenze di campionamento fino a 48 KHz e velocità in bit massima di 161 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="db52b-118">L3</span><span class="sxs-lookup"><span data-stu-id="db52b-118">"L3"</span></span>  | <span data-ttu-id="db52b-119">Codifica standard con frequenze di campionamento fino a 48 KHz e velocità in bit massima di 385 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="db52b-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="db52b-120">"M0a"</span></span> | <span data-ttu-id="db52b-121">Codifica professionale con frequenze di campionamento fino a 48 KHz e velocità in bit comprese tra 48 e 192 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="db52b-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="db52b-122">"M0b"</span></span> | <span data-ttu-id="db52b-123">Codifica professionale con frequenza di campionamento fino a 48 KHz e velocità in bit massima di 192 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="db52b-124">M1</span><span class="sxs-lookup"><span data-stu-id="db52b-124">"M1"</span></span>  | <span data-ttu-id="db52b-125">Codifica professionale con frequenza di campionamento fino a 48 KHz e velocità in bit massima di 384 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="db52b-126">M2</span><span class="sxs-lookup"><span data-stu-id="db52b-126">"M2"</span></span>  | <span data-ttu-id="db52b-127">Codifica professionale con frequenza di campionamento fino a 96 KHz e velocità in bit massima di 768 kbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="db52b-128">M3</span><span class="sxs-lookup"><span data-stu-id="db52b-128">"M3"</span></span>  | <span data-ttu-id="db52b-129">Codifica professionale con frequenza di campionamento fino a 96 KHz e velocità in bit massima di 1,5 Mbps.</span><span class="sxs-lookup"><span data-stu-id="db52b-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="db52b-130">N1</span><span class="sxs-lookup"><span data-stu-id="db52b-130">"N1"</span></span>  | <span data-ttu-id="db52b-131">Codifica senza perdita di frequenza con frequenze di campionamento fino a 48 KHz e un massimo di 2 canali.</span><span class="sxs-lookup"><span data-stu-id="db52b-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="db52b-132">N2</span><span class="sxs-lookup"><span data-stu-id="db52b-132">"N2"</span></span>  | <span data-ttu-id="db52b-133">Codifica senza perdita di frequenza con frequenze di campionamento fino a 96 KHz e un massimo di 6 canali (surround 5,1).</span><span class="sxs-lookup"><span data-stu-id="db52b-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="db52b-134">N3</span><span class="sxs-lookup"><span data-stu-id="db52b-134">"N3"</span></span>  | <span data-ttu-id="db52b-135">Codifica senza perdita di frequenza con frequenze di campionamento fino a 96 KHz e un massimo di 8 canali (7,1 surround).</span><span class="sxs-lookup"><span data-stu-id="db52b-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="db52b-136">Per il video, questa proprietà ha uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="db52b-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="db52b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="db52b-137">Value</span></span> | <span data-ttu-id="db52b-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db52b-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="db52b-139">Asia Pacifico</span><span class="sxs-lookup"><span data-stu-id="db52b-139">"AP"</span></span>  | <span data-ttu-id="db52b-140">profilo avanzato (disponibile solo in Windows Media Video 9 Advanced Profile codec)</span><span class="sxs-lookup"><span data-stu-id="db52b-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="db52b-141">CP</span><span class="sxs-lookup"><span data-stu-id="db52b-141">"CP"</span></span>  | <span data-ttu-id="db52b-142">non più supportato</span><span class="sxs-lookup"><span data-stu-id="db52b-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="db52b-143">MP</span><span class="sxs-lookup"><span data-stu-id="db52b-143">"MP"</span></span>  | <span data-ttu-id="db52b-144">profilo principale</span><span class="sxs-lookup"><span data-stu-id="db52b-144">main profile</span></span>                                                                      |
| <span data-ttu-id="db52b-145">SP</span><span class="sxs-lookup"><span data-stu-id="db52b-145">"SP"</span></span>  | <span data-ttu-id="db52b-146">Profilo semplice</span><span class="sxs-lookup"><span data-stu-id="db52b-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="db52b-147">Per il contenuto video, è possibile richiedere un livello di profilo impostando [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) prima di iniziare la codifica.</span><span class="sxs-lookup"><span data-stu-id="db52b-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="db52b-148">Il codec tenterà di codificare entro i parametri del livello di complessità richiesto, ma le altre impostazioni configurate avranno la precedenza.</span><span class="sxs-lookup"><span data-stu-id="db52b-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="db52b-149">È consigliabile controllare sempre il valore del profilo di complessità effettivo dopo la codifica nel caso in cui non sia possibile rispettare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="db52b-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="db52b-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db52b-150">Requirements</span></span>



| <span data-ttu-id="db52b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="db52b-151">Requirement</span></span> | <span data-ttu-id="db52b-152">Valore</span><span class="sxs-lookup"><span data-stu-id="db52b-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db52b-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db52b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="db52b-154">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="db52b-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db52b-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db52b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="db52b-156">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db52b-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db52b-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db52b-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="db52b-158"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db52b-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db52b-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db52b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db52b-160">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db52b-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




