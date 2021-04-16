---
description: Specifica il formato di output per il decodificatore.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Proprietà AVDecCommonOutputFormat (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522481"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="ef78e-103">Proprietà AVDecCommonOutputFormat</span><span class="sxs-lookup"><span data-stu-id="ef78e-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="ef78e-104">Specifica il formato di output per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="ef78e-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="ef78e-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ef78e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ef78e-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ef78e-106">Data type</span></span>

<span data-ttu-id="ef78e-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="ef78e-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ef78e-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="ef78e-108">Property GUID</span></span>

<span data-ttu-id="ef78e-109">**Codecapis \_ AVDecCommonOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="ef78e-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="ef78e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ef78e-110">Property value</span></span>



| <span data-ttu-id="ef78e-111">GUID</span><span class="sxs-lookup"><span data-stu-id="ef78e-111">GUID</span></span>                                                               | <span data-ttu-id="ef78e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef78e-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef78e-113">AVDecAudioOutputFormat GUID codecapis \_ \_ \_ PCM</span><span class="sxs-lookup"><span data-stu-id="ef78e-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="ef78e-114">Audio PCM, usando un numero qualsiasi di canali</span><span class="sxs-lookup"><span data-stu-id="ef78e-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="ef78e-115">\_ \_ Cuffie AVDecAudioOutputFormat GUID \_ \_ di codecapi</span><span class="sxs-lookup"><span data-stu-id="ef78e-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="ef78e-116">Audio PCM stereo, usando solo a sinistra/a destra (lo/ro) downmix</span><span class="sxs-lookup"><span data-stu-id="ef78e-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="ef78e-117">Codecapis \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stereo \_ auto</span><span class="sxs-lookup"><span data-stu-id="ef78e-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="ef78e-118">Audio PCM stereo, usando la selezione automatica della modalità downmix stereo (lo/ro o LT/RT).</span><span class="sxs-lookup"><span data-stu-id="ef78e-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="ef78e-119">È possibile usare questo valore per formati audio in cui il flusso di input definisce la modalità downmix preferita, ad esempio Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="ef78e-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="ef78e-120">Codecapis \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stereo \_ MatrixEncoded</span><span class="sxs-lookup"><span data-stu-id="ef78e-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="ef78e-121">Audio PCM stereo, uso di downmix stereo con codifica Matrix (LT/RT)</span><span class="sxs-lookup"><span data-stu-id="ef78e-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="ef78e-122">\_ \_ Bitstream GUID AVDecAudioOutputFormat \_ SPDIF \_</span><span class="sxs-lookup"><span data-stu-id="ef78e-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="ef78e-123">Bitstream compresso S/PDIF (Sony/Philips Digital Interface Format), come definito da IEC-60958</span><span class="sxs-lookup"><span data-stu-id="ef78e-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="ef78e-124">Codecapis \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="ef78e-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="ef78e-125">Stereo PCM S/PDIF, come definito da IEC-60958</span><span class="sxs-lookup"><span data-stu-id="ef78e-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="ef78e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef78e-126">Requirements</span></span>



| <span data-ttu-id="ef78e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef78e-127">Requirement</span></span> | <span data-ttu-id="ef78e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ef78e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef78e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef78e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ef78e-130">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="ef78e-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ef78e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef78e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ef78e-132">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ef78e-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ef78e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef78e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef78e-134"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef78e-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef78e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef78e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef78e-136">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="ef78e-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ef78e-137">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ef78e-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




