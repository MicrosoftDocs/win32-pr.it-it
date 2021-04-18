---
description: Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da MFPKEY \_ Rmax).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Proprietà MFPKEY_BMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318403"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="a8b65-103">\_Proprietà BMAX di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="a8b65-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="a8b65-104">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="a8b65-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a8b65-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a8b65-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a8b65-106">g \_ wszWMVCBMax</span><span class="sxs-lookup"><span data-stu-id="a8b65-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="a8b65-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a8b65-107">Data Type</span></span>

<span data-ttu-id="a8b65-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a8b65-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a8b65-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="a8b65-109">Default Value</span></span>

<span data-ttu-id="a8b65-110">Nessuna impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8b65-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b65-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8b65-111">Remarks</span></span>

<span data-ttu-id="a8b65-112">È necessario impostare questo valore per la codifica VBR con vincoli di picco.</span><span class="sxs-lookup"><span data-stu-id="a8b65-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="a8b65-113">Dopo aver iniziato l'elaborazione degli esempi, non è necessario eseguire una query per questo valore fino a quando non si termina la codifica del flusso.</span><span class="sxs-lookup"><span data-stu-id="a8b65-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="a8b65-114">Il codec interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica; L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="a8b65-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b65-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b65-115">Requirements</span></span>



| <span data-ttu-id="a8b65-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b65-116">Requirement</span></span> | <span data-ttu-id="a8b65-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b65-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b65-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b65-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b65-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8b65-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a8b65-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b65-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b65-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8b65-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8b65-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8b65-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b65-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b65-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b65-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8b65-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b65-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8b65-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




