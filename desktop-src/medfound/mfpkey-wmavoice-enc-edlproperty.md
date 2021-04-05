---
description: Specifica le parti di contenuto da codificare come musica dal codec vocale.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Proprietà MFPKEY_WMAVOICE_ENC_EDL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755306"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="be688-103">MFPKEY \_ WMAVOICE \_ enc ( \_ Proprietà EDL)</span><span class="sxs-lookup"><span data-stu-id="be688-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="be688-104">Specifica le parti di contenuto da codificare come musica dal codec vocale.</span><span class="sxs-lookup"><span data-stu-id="be688-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="be688-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="be688-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="be688-106">g \_ wszWMACVoiceBuffer</span><span class="sxs-lookup"><span data-stu-id="be688-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="be688-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="be688-107">Data Type</span></span>

<span data-ttu-id="be688-108">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="be688-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="be688-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="be688-109">Default Value</span></span>

<span data-ttu-id="be688-110">Nessun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="be688-110">No default value.</span></span> <span data-ttu-id="be688-111">Se questa proprietà non è impostata, il codec utilizzerà il valore della proprietà [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) per determinare come codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="be688-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="be688-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="be688-112">Remarks</span></span>

<span data-ttu-id="be688-113">È possibile usare questa proprietà se la modalità automatica del codec non fornisce risultati soddisfacenti.</span><span class="sxs-lookup"><span data-stu-id="be688-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="be688-114">Questo valore è una stringa delimitata da virgole che contiene almeno quattro numeri interi.</span><span class="sxs-lookup"><span data-stu-id="be688-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="be688-115">Il primo valore integer è il numero di versione; usare sempre 1 per questo valore.</span><span class="sxs-lookup"><span data-stu-id="be688-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="be688-116">Il secondo Integer è il numero di sezioni che devono essere codificate come musica.</span><span class="sxs-lookup"><span data-stu-id="be688-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="be688-117">Il secondo numero intero è costituito da un numero di coppie di valori che rappresentano intervalli in millisecondi, una coppia per ogni sezione di contenuto che deve essere codificata come musica.</span><span class="sxs-lookup"><span data-stu-id="be688-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="be688-118">Ad esempio, "1, 2100200500600" informa il codificatore di usare la versione 1 con due sezioni di musica.</span><span class="sxs-lookup"><span data-stu-id="be688-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="be688-119">La prima sezione Music inizia a 100 ms e termina con 200 ms.</span><span class="sxs-lookup"><span data-stu-id="be688-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="be688-120">La seconda sezione Music inizia a 500 ms e termina con 600 ms.</span><span class="sxs-lookup"><span data-stu-id="be688-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="be688-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be688-121">Requirements</span></span>



| <span data-ttu-id="be688-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="be688-122">Requirement</span></span> | <span data-ttu-id="be688-123">Valore</span><span class="sxs-lookup"><span data-stu-id="be688-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be688-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be688-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be688-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be688-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="be688-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be688-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be688-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be688-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be688-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be688-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be688-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be688-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be688-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be688-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be688-131">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be688-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




