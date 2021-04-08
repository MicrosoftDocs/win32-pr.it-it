---
description: Specifica una rappresentazione numerica del compromesso tra la fluidità del movimento e la qualità dell'immagine dell'output del codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Proprietà MFPKEY_CRISP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755487"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="113b4-103">MFPKEY ( \_ Proprietà croccante)</span><span class="sxs-lookup"><span data-stu-id="113b4-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="113b4-104">Specifica una rappresentazione numerica del compromesso tra la fluidità del movimento e la qualità dell'immagine dell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="113b4-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="113b4-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="113b4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="113b4-106">g \_ wszWMVCCrisp</span><span class="sxs-lookup"><span data-stu-id="113b4-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="113b4-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="113b4-107">Data Type</span></span>

<span data-ttu-id="113b4-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="113b4-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="113b4-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="113b4-109">Default Value</span></span>

<span data-ttu-id="113b4-110">75</span><span class="sxs-lookup"><span data-stu-id="113b4-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="113b4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="113b4-111">Remarks</span></span>

<span data-ttu-id="113b4-112">Questo valore integer può variare da 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="113b4-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="113b4-113">Maggiore è il valore, maggiore sarà il codec per ottimizzare la codifica per la qualità dell'immagine dei singoli frame, che in genere riduce la fluidità del movimento.</span><span class="sxs-lookup"><span data-stu-id="113b4-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="113b4-114">Questa proprietà deve essere impostata solo per la codifica di velocità in bit costante (CBR).</span><span class="sxs-lookup"><span data-stu-id="113b4-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="113b4-115">Le ottimizzazioni per la codifica con velocità in bit variabile (VBR) funzionano in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="113b4-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="113b4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113b4-116">Requirements</span></span>



| <span data-ttu-id="113b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="113b4-117">Requirement</span></span> | <span data-ttu-id="113b4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="113b4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="113b4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="113b4-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="113b4-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="113b4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="113b4-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="113b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="113b4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="113b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="113b4-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="113b4-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="113b4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113b4-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="113b4-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




