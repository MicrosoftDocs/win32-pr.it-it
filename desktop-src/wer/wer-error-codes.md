---
title: Codici di errore WER (Werapi. h)
description: Nella tabella seguente viene fornito un elenco di codici di errore personalizzati utilizzati da Segnalazione errori Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301536"
---
# <a name="wer-error-codes"></a><span data-ttu-id="67fa4-103">Codici di errore WER</span><span class="sxs-lookup"><span data-stu-id="67fa4-103">WER Error Codes</span></span>

<span data-ttu-id="67fa4-104">Nella tabella seguente viene fornito un elenco di codici di errore personalizzati utilizzati da Segnalazione errori Windows.</span><span class="sxs-lookup"><span data-stu-id="67fa4-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="67fa4-105">Costante</span><span class="sxs-lookup"><span data-stu-id="67fa4-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="67fa4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67fa4-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="67fa4-107"><dt>**BUFFER di WER \_ E \_ insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="67fa4-108">Un buffer è troppo piccolo per contenere i dati.</span><span class="sxs-lookup"><span data-stu-id="67fa4-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="67fa4-109"><dt>**\_stato wer E \_ non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="67fa4-110">Una funzione è stata chiamata in modo non supportato.</span><span class="sxs-lookup"><span data-stu-id="67fa4-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="67fa4-111"><dt>**lunghezza di WER \_ E \_ \_ superata**</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="67fa4-112">È stato superato uno dei limiti di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="67fa4-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="67fa4-113"><dt>**\_parametro wer E \_ mancante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="67fa4-114">Uno o più parametri mancanti.</span><span class="sxs-lookup"><span data-stu-id="67fa4-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="67fa4-115"><dt>**WER \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="67fa4-116">Element not found.</span><span class="sxs-lookup"><span data-stu-id="67fa4-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="67fa4-117"><dt>**WER \_ E \_ Store \_ disabilitato**</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="67fa4-118">L'archivio è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="67fa4-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="67fa4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67fa4-119">Requirements</span></span>



| <span data-ttu-id="67fa4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="67fa4-120">Requirement</span></span> | <span data-ttu-id="67fa4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="67fa4-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="67fa4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67fa4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67fa4-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67fa4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="67fa4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67fa4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67fa4-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67fa4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="67fa4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67fa4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67fa4-127"><dt>Werapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67fa4-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 





