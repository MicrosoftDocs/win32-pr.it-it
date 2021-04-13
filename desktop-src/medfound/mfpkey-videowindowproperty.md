---
description: Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: Proprietà MFPKEY_VIDEOWINDOW (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527966"
---
# <a name="mfpkey_videowindow-property"></a><span data-ttu-id="6fa06-103">\_Proprietà VIDEOWINDOW di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="6fa06-103">MFPKEY\_VIDEOWINDOW Property</span></span>

<span data-ttu-id="6fa06-104">Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.</span><span class="sxs-lookup"><span data-stu-id="6fa06-104">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6fa06-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6fa06-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6fa06-106">g \_ wszWMVCVideoWIndow</span><span class="sxs-lookup"><span data-stu-id="6fa06-106">g\_wszWMVCVideoWIndow</span></span>

## <a name="data-type"></a><span data-ttu-id="6fa06-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6fa06-107">Data Type</span></span>

<span data-ttu-id="6fa06-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6fa06-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="6fa06-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="6fa06-109">Default Value</span></span>

<span data-ttu-id="6fa06-110">3000</span><span class="sxs-lookup"><span data-stu-id="6fa06-110">3000</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa06-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fa06-111">Remarks</span></span>

<span data-ttu-id="6fa06-112">La finestra buffer è uno dei parametri del modello "leaky bucket" usato nel controllo della frequenza del codec.</span><span class="sxs-lookup"><span data-stu-id="6fa06-112">The buffer window is one of the "leaky bucket" model parameters used in the codec rate control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa06-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fa06-113">Requirements</span></span>



| <span data-ttu-id="6fa06-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa06-114">Requirement</span></span> | <span data-ttu-id="6fa06-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6fa06-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa06-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fa06-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa06-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6fa06-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6fa06-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fa06-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa06-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fa06-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6fa06-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fa06-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa06-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa06-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa06-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fa06-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa06-123">Configurazione della codifica video</span><span class="sxs-lookup"><span data-stu-id="6fa06-123">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="6fa06-124">Modello di buffer di bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="6fa06-124">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="6fa06-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6fa06-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




