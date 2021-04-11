---
description: Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Proprietà MFPKEY_PRODUCEDUMMYFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226995"
---
# <a name="mfpkey_producedummyframes-property"></a><span data-ttu-id="3f19a-103">\_Proprietà PRODUCEDUMMYFRAMES di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="3f19a-103">MFPKEY\_PRODUCEDUMMYFRAMES Property</span></span>

<span data-ttu-id="3f19a-104">Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.</span><span class="sxs-lookup"><span data-stu-id="3f19a-104">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3f19a-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3f19a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3f19a-106">g \_ wszWMVCProduceDummyFrames</span><span class="sxs-lookup"><span data-stu-id="3f19a-106">g\_wszWMVCProduceDummyFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="3f19a-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3f19a-107">Data Type</span></span>

<span data-ttu-id="3f19a-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="3f19a-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="3f19a-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3f19a-109">Default Value</span></span>

<span data-ttu-id="3f19a-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="3f19a-110">VARIANT\_FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="3f19a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f19a-111">Remarks</span></span>

<span data-ttu-id="3f19a-112">Se questo valore è VARIANT \_ false, il codec non inserisce i dati nel flusso di bit per i frame duplicati.</span><span class="sxs-lookup"><span data-stu-id="3f19a-112">If this value is VARIANT\_FALSE, the codec will not put any data in the bit stream for duplicate frames.</span></span>

<span data-ttu-id="3f19a-113">I frame fittizi possono essere importanti nelle applicazioni in cui i numeri dei frame sono salvati in permanenza.</span><span class="sxs-lookup"><span data-stu-id="3f19a-113">Dummy frames can be important in applications where frame numbers are persisted.</span></span> <span data-ttu-id="3f19a-114">Un esempio comune è quando vengono conservati i codici temporali SMPTE per il contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="3f19a-114">A common example is when SMPTE time codes are maintained for encoded content.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f19a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f19a-115">Requirements</span></span>



| <span data-ttu-id="3f19a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f19a-116">Requirement</span></span> | <span data-ttu-id="3f19a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3f19a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f19a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f19a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f19a-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3f19a-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3f19a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f19a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f19a-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f19a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f19a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f19a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f19a-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f19a-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f19a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f19a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f19a-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f19a-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




