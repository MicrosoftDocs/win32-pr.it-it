---
description: Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Proprietà MFPKEY_CODEDNONZEROFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311583"
---
# <a name="mfpkey_codednonzeroframes-property"></a><span data-ttu-id="bf90d-103">\_Proprietà CODEDNONZEROFRAMES di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="bf90d-103">MFPKEY\_CODEDNONZEROFRAMES Property</span></span>

<span data-ttu-id="bf90d-104">Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.</span><span class="sxs-lookup"><span data-stu-id="bf90d-104">Specifies the number of video frames encoded by the codec that actually contain data.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bf90d-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="bf90d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="bf90d-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="bf90d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="bf90d-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bf90d-107">Data Type</span></span>

<span data-ttu-id="bf90d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="bf90d-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="bf90d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf90d-109">Remarks</span></span>

<span data-ttu-id="bf90d-110">Questo valore è uguale a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) meno tutti i frame eliminati a causa di vincoli di velocità di bit, meno qualsiasi frame di zero byte.</span><span class="sxs-lookup"><span data-stu-id="bf90d-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints, minus any zero-byte frames.</span></span> <span data-ttu-id="bf90d-111">È possibile ottenere questo valore al termine del passaggio degli esempi.</span><span class="sxs-lookup"><span data-stu-id="bf90d-111">You can get this value after you are finished passing samples.</span></span> <span data-ttu-id="bf90d-112">I frame a zero byte possono essere creati per i frame duplicati.</span><span class="sxs-lookup"><span data-stu-id="bf90d-112">Zero-byte frames can be created for duplicate frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf90d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf90d-113">Requirements</span></span>



| <span data-ttu-id="bf90d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf90d-114">Requirement</span></span> | <span data-ttu-id="bf90d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bf90d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf90d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf90d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf90d-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bf90d-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bf90d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf90d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf90d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf90d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf90d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf90d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf90d-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf90d-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf90d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf90d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf90d-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf90d-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
