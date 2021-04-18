---
description: Specifica la modalità del codec vocale.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Proprietà MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309108"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="ca628-103">\_Proprietà MFPKEY WMAVOICE \_ enc \_ MusicSpeechClassMode</span><span class="sxs-lookup"><span data-stu-id="ca628-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="ca628-104">Specifica la modalità del codec vocale.</span><span class="sxs-lookup"><span data-stu-id="ca628-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ca628-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ca628-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ca628-106">g \_ wszWMACMusicSpeechClassMode</span><span class="sxs-lookup"><span data-stu-id="ca628-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="ca628-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ca628-107">Data Type</span></span>

<span data-ttu-id="ca628-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ca628-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ca628-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="ca628-109">Default Value</span></span>

<span data-ttu-id="ca628-110">1</span><span class="sxs-lookup"><span data-stu-id="ca628-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="ca628-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca628-111">Remarks</span></span>

<span data-ttu-id="ca628-112">Il valore 1 informa il codec che il contenuto è di sola voce, il valore 2 indica che il codec determina automaticamente la modalità e qualsiasi altro valore informa il codec per l'utilizzo della modalità musica.</span><span class="sxs-lookup"><span data-stu-id="ca628-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="ca628-113">Se la modalità automatica non codifica la voce mista e la musica in modo corretto, è possibile specificare la codifica per le singole sezioni del file usando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ca628-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca628-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca628-114">Requirements</span></span>



| <span data-ttu-id="ca628-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca628-115">Requirement</span></span> | <span data-ttu-id="ca628-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ca628-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca628-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca628-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca628-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ca628-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ca628-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca628-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca628-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca628-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca628-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca628-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca628-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca628-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca628-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca628-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca628-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca628-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




