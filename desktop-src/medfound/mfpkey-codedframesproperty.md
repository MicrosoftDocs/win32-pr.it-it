---
description: Specifica il numero di fotogrammi video codificati dal codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Proprietà MFPKEY_CODEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314022"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="03db2-103">\_Proprietà CODEDFRAMES di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="03db2-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="03db2-104">Specifica il numero di fotogrammi video codificati dal codec.</span><span class="sxs-lookup"><span data-stu-id="03db2-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="03db2-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="03db2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="03db2-106">g \_ wszWMVCCodedFrames</span><span class="sxs-lookup"><span data-stu-id="03db2-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="03db2-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="03db2-107">Data Type</span></span>

<span data-ttu-id="03db2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="03db2-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="03db2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="03db2-109">Remarks</span></span>

<span data-ttu-id="03db2-110">Questo valore è uguale a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) meno tutti i frame eliminati a causa di vincoli di velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="03db2-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="03db2-111">È possibile ottenere questo valore al termine del passaggio degli esempi.</span><span class="sxs-lookup"><span data-stu-id="03db2-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="03db2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03db2-112">Requirements</span></span>



| <span data-ttu-id="03db2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="03db2-113">Requirement</span></span> | <span data-ttu-id="03db2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="03db2-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03db2-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03db2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="03db2-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="03db2-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03db2-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03db2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="03db2-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03db2-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03db2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03db2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="03db2-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03db2-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03db2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03db2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03db2-122">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03db2-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




