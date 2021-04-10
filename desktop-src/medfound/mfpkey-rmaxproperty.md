---
description: Specifica la velocità in bit del picco, in bit al secondo, usata per la riproduzione con frequenza in bit (VBR) a 2 passaggi vincolata.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Proprietà MFPKEY_RMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226977"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="94c9c-103">\_Proprietà Rmax di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="94c9c-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="94c9c-104">Specifica la velocità in bit del picco, in bit al secondo, usata per la riproduzione con frequenza in bit (VBR) a 2 passaggi vincolata.</span><span class="sxs-lookup"><span data-stu-id="94c9c-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="94c9c-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="94c9c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="94c9c-106">g \_ wszWMVCMaxBitrate</span><span class="sxs-lookup"><span data-stu-id="94c9c-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="94c9c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="94c9c-107">Data Type</span></span>

<span data-ttu-id="94c9c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="94c9c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="94c9c-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="94c9c-109">Default Value</span></span>

<span data-ttu-id="94c9c-110">Nessuna impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="94c9c-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="94c9c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="94c9c-111">Remarks</span></span>

<span data-ttu-id="94c9c-112">Questo valore rappresenta la velocità in bit massima per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="94c9c-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="94c9c-113">Il valore di [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) viene usato per descrivere il buffer in base a questa velocità in bit. in effetti, il formato VBR vincolato è simile alla velocità in bit costante (CBR) che usa questo valore come velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="94c9c-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="94c9c-114">Tuttavia, un flusso VBR vincolato può essere riprodotto a una velocità in bit inferiore, a condizione che il buffer venga aumentato.</span><span class="sxs-lookup"><span data-stu-id="94c9c-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="94c9c-115">È necessario impostare questo valore per la codifica VBR a due passaggi con vincoli di picco.</span><span class="sxs-lookup"><span data-stu-id="94c9c-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="94c9c-116">Dopo aver iniziato l'elaborazione degli esempi, non è necessario eseguire una query per questo valore fino a quando non si termina la codifica del flusso.</span><span class="sxs-lookup"><span data-stu-id="94c9c-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="94c9c-117">Il codificatore interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica. L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="94c9c-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="94c9c-118">In genere, questo valore è da due a tre volte maggiore del valore di [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="94c9c-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94c9c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94c9c-119">Requirements</span></span>



| <span data-ttu-id="94c9c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="94c9c-120">Requirement</span></span> | <span data-ttu-id="94c9c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="94c9c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94c9c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94c9c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94c9c-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94c9c-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="94c9c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94c9c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94c9c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94c9c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94c9c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94c9c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="94c9c-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94c9c-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c9c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94c9c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c9c-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94c9c-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




