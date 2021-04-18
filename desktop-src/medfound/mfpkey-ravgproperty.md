---
description: Specifica la velocità in bit media, in bit al secondo, usata per la codifica a una velocità in bit (VBR) a 2 passaggi.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Proprietà MFPKEY_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310618"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="41c33-103">\_Proprietà RAVG di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="41c33-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="41c33-104">Specifica la velocità in bit media, in bit al secondo, usata per la codifica a una velocità in bit (VBR) a 2 passaggi.</span><span class="sxs-lookup"><span data-stu-id="41c33-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="41c33-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="41c33-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="41c33-106">g \_ wszWMVCAvgBitrate</span><span class="sxs-lookup"><span data-stu-id="41c33-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="41c33-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="41c33-107">Data Type</span></span>

<span data-ttu-id="41c33-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="41c33-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="41c33-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="41c33-109">Remarks</span></span>

<span data-ttu-id="41c33-110">In un VBR vincolato e non vincolato, questo valore corrisponde alla velocità in bit media per tutta la durata del contenuto.</span><span class="sxs-lookup"><span data-stu-id="41c33-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="41c33-111">È necessario impostare questo valore per entrambe le modalità di codifica VBR a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="41c33-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="41c33-112">Dopo aver iniziato l'elaborazione degli esempi, non è necessario eseguire una query per questo valore fino a quando non si termina la codifica del flusso.</span><span class="sxs-lookup"><span data-stu-id="41c33-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="41c33-113">Il codificatore interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica. L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="41c33-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="41c33-114">Questa proprietà può essere letta anche alla fine di una sessione di codifica VBR da 1 pass.</span><span class="sxs-lookup"><span data-stu-id="41c33-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c33-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41c33-115">Requirements</span></span>



| <span data-ttu-id="41c33-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c33-116">Requirement</span></span> | <span data-ttu-id="41c33-117">Valore</span><span class="sxs-lookup"><span data-stu-id="41c33-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c33-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c33-118">Minimum supported client</span></span><br/> | <span data-ttu-id="41c33-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="41c33-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="41c33-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c33-120">Minimum supported server</span></span><br/> | <span data-ttu-id="41c33-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41c33-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41c33-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41c33-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c33-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c33-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c33-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41c33-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c33-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41c33-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




