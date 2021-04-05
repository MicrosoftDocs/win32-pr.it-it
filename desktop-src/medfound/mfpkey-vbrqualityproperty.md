---
description: Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: Proprietà MFPKEY_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967162"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="9d08f-103">\_Proprietà VBRQUALITY di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="9d08f-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="9d08f-104">Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).</span><span class="sxs-lookup"><span data-stu-id="9d08f-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9d08f-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9d08f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9d08f-106">g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality</span><span class="sxs-lookup"><span data-stu-id="9d08f-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="9d08f-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9d08f-107">Data Type</span></span>

<span data-ttu-id="9d08f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9d08f-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="9d08f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d08f-109">Remarks</span></span>

<span data-ttu-id="9d08f-110">Non tutti i valori nell'intervallo hanno un significato univoco.</span><span class="sxs-lookup"><span data-stu-id="9d08f-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="9d08f-111">I valori che rappresentano un passaggio di qualità rispetto al livello precedente sono: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 e 100.</span><span class="sxs-lookup"><span data-stu-id="9d08f-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="9d08f-112">Per gli oggetti del codificatore audio, le modalità di qualità vengono fornite nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dei tipi di output recuperati tramite [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="9d08f-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d08f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d08f-113">Requirements</span></span>



| <span data-ttu-id="9d08f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d08f-114">Requirement</span></span> | <span data-ttu-id="9d08f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9d08f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d08f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d08f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d08f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d08f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9d08f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d08f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d08f-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d08f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d08f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d08f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d08f-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d08f-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d08f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d08f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d08f-123">Enumerazione dei tipi audio per modalità di codifica specifiche</span><span class="sxs-lookup"><span data-stu-id="9d08f-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="9d08f-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9d08f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
