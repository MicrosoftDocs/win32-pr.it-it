---
description: Imposta come attributo per un oggetto IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Attributo MFPROTECTIONATTRIBUTE_BEST_EFFORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226913"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="ec89c-103">\_Attributo MFPROTECTIONATTRIBUTE Best \_ effort</span><span class="sxs-lookup"><span data-stu-id="ec89c-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="ec89c-104">Imposta come attributo per un oggetto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="ec89c-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="ec89c-105">Se questo attributo è presente, un tentativo non riuscito di applicare la protezione viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec89c-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="ec89c-106">Se il valore dell'attributo associato è **true**, deve essere applicato lo schema di protezione con l'attributo di [ \_ failover \_ MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) .</span><span class="sxs-lookup"><span data-stu-id="ec89c-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="ec89c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ec89c-107">Data type</span></span>

<span data-ttu-id="ec89c-108">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec89c-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ec89c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec89c-109">Remarks</span></span>

<span data-ttu-id="ec89c-110">Se **true**, applica lo schema di protezione con l'attributo di [ \_ failover MFPROTECTIONATTRIBUTE \_](mfprotectionattribute-fail-over.md) se l'impostazione di questa protezione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ec89c-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="ec89c-111">Imposta come attributo per un oggetto [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="ec89c-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec89c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec89c-112">Requirements</span></span>



| <span data-ttu-id="ec89c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec89c-113">Requirement</span></span> | <span data-ttu-id="ec89c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ec89c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec89c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec89c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec89c-116">\[Solo app UWP Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ec89c-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ec89c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec89c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec89c-118">\[Solo app UWP Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ec89c-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ec89c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec89c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec89c-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec89c-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec89c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec89c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec89c-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec89c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec89c-123">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="ec89c-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




