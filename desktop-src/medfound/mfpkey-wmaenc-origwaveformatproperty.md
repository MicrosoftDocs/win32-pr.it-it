---
description: Specifica la struttura WAVEFORMATEX che descrive il contenuto audio di input.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Proprietà MFPKEY_WMAENC_ORIGWAVEFORMAT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226915"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="a0f21-103">MFPKEY \_ WMAENC- \_ Proprietà ORIGWAVEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a0f21-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="a0f21-104">Specifica la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che descrive il contenuto audio di input.</span><span class="sxs-lookup"><span data-stu-id="a0f21-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a0f21-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a0f21-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a0f21-106">g \_ wszWMACOriginalWaveFormat</span><span class="sxs-lookup"><span data-stu-id="a0f21-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="a0f21-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a0f21-107">Data Type</span></span>

<span data-ttu-id="a0f21-108">VT \_ array \| VT \_ Ui1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) come matrice di byte)</span><span class="sxs-lookup"><span data-stu-id="a0f21-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f21-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f21-109">Remarks</span></span>

<span data-ttu-id="a0f21-110">Quando si esegue la transcodifica di contenuto basato su Windows Media Audio a una velocità in bit inferiore, è possibile passare la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del contenuto al codec per consentire al codec di ottimizzare gli algoritmi.</span><span class="sxs-lookup"><span data-stu-id="a0f21-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="a0f21-111">Questa funzionalità, denominata ricompressione intelligente, fornisce risultati migliori rispetto alla decompressione del contenuto e quindi all'inserimento dei campioni PCM ricostruiti tramite il codec.</span><span class="sxs-lookup"><span data-stu-id="a0f21-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="a0f21-112">Quando si passa la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , includere eventuali byte aggiuntivi alla fine della struttura specificata da **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="a0f21-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="a0f21-113">Il codificatore audio accetta solo gli input e gli output per i quali il numero di canali, i bit per campione e la frequenza di campionamento sono identici.</span><span class="sxs-lookup"><span data-stu-id="a0f21-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="a0f21-114">È possibile transcodificare il contenuto solo a una velocità in bit inferiore all'interno di tali parametri.</span><span class="sxs-lookup"><span data-stu-id="a0f21-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="a0f21-115">In ogni caso, è necessario decodificare il contenuto e passare gli esempi non compressi come input al codificatore.</span><span class="sxs-lookup"><span data-stu-id="a0f21-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="a0f21-116">L'impostazione di questa proprietà fornisce al codificatore alcune informazioni sull'elaborazione già eseguita sul contenuto.</span><span class="sxs-lookup"><span data-stu-id="a0f21-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f21-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f21-117">Requirements</span></span>



| <span data-ttu-id="a0f21-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f21-118">Requirement</span></span> | <span data-ttu-id="a0f21-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f21-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f21-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0f21-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f21-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0f21-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0f21-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0f21-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f21-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0f21-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0f21-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f21-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f21-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f21-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f21-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f21-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a0f21-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
