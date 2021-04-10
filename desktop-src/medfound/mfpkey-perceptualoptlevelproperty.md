---
description: Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Proprietà MFPKEY_PERCEPTUALOPTLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226998"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="d89fb-103">\_Proprietà PERCEPTUALOPTLEVEL di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="d89fb-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="d89fb-104">Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="d89fb-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d89fb-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d89fb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d89fb-106">g \_ wszWMVCPerceptualOptLevel</span><span class="sxs-lookup"><span data-stu-id="d89fb-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="d89fb-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d89fb-107">Data Type</span></span>

<span data-ttu-id="d89fb-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d89fb-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d89fb-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="d89fb-109">Default Value</span></span>

<span data-ttu-id="d89fb-110">0</span><span class="sxs-lookup"><span data-stu-id="d89fb-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="d89fb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d89fb-111">Remarks</span></span>

<span data-ttu-id="d89fb-112">L'ottimizzazione percettiva conservativa è un processo mediante il quale il codec tenta di identificare le aree "importanti" e "non importanti" nel frame del video.</span><span class="sxs-lookup"><span data-stu-id="d89fb-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="d89fb-113">Dopo aver identificato queste aree del frame, il codec fornirà una priorità più elevata alla qualità delle aree importanti, a scapito della qualità delle aree non importanti.</span><span class="sxs-lookup"><span data-stu-id="d89fb-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="d89fb-114">L'ottimizzazione percettiva enfatizza l'aspetto dell'immagine come corretta per gli occhi umani, anziché insistere su una rigorosa precisione matematica.</span><span class="sxs-lookup"><span data-stu-id="d89fb-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="d89fb-115">I risultati dell'ottimizzazione variano notevolmente a seconda del tipo di video da codificare.</span><span class="sxs-lookup"><span data-stu-id="d89fb-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="d89fb-116">Questa funzionalità può essere adatta per la codifica a bassa velocità di bit e bassa risoluzione (ad esempio, lo streaming web), ma dovrebbe essere evitata quando si mira alla qualità del video di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d89fb-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="d89fb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d89fb-117">Requirements</span></span>



| <span data-ttu-id="d89fb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89fb-118">Requirement</span></span> | <span data-ttu-id="d89fb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d89fb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d89fb-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d89fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d89fb-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d89fb-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d89fb-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d89fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d89fb-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d89fb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d89fb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d89fb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d89fb-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89fb-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89fb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d89fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89fb-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d89fb-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




