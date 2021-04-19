---
description: Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit media (specificata da MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Proprietà MFPKEY_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311589"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="25949-103">\_Proprietà BAVG di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="25949-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="25949-104">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit media (specificata da [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="25949-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="25949-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="25949-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="25949-106">g \_ wszWMVCBAvg</span><span class="sxs-lookup"><span data-stu-id="25949-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="25949-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="25949-107">Data Type</span></span>

<span data-ttu-id="25949-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="25949-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="25949-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="25949-109">Default Value</span></span>

<span data-ttu-id="25949-110">Nessun valore predefinito, ma il codec calcolerà un valore appropriato in base alle altre impostazioni VBR vincolate.</span><span class="sxs-lookup"><span data-stu-id="25949-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="25949-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="25949-111">Remarks</span></span>

<span data-ttu-id="25949-112">Questo valore viene calcolato dal codec dopo il passaggio di codifica finale.</span><span class="sxs-lookup"><span data-stu-id="25949-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="25949-113">Non eseguire una query per questo valore fino al completamento della codifica.</span><span class="sxs-lookup"><span data-stu-id="25949-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="25949-114">Il codec interpreta una richiesta di questo valore come segnale del superamento della sessione di codifica; L'esempio successivo elaborato viene considerato come l'inizio di una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="25949-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="25949-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25949-115">Requirements</span></span>



| <span data-ttu-id="25949-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25949-116">Requirement</span></span> | <span data-ttu-id="25949-117">Valore</span><span class="sxs-lookup"><span data-stu-id="25949-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25949-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25949-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25949-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="25949-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25949-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25949-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25949-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25949-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25949-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25949-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25949-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25949-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25949-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25949-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25949-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25949-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




