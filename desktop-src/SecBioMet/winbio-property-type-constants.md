---
title: Costanti WINBIO_PROPERTY_TYPE (WinBio. h)
description: Specificare l'origine delle informazioni sulle proprietà nella funzione WinBioGetProperty.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479252"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="6eb4b-103">Costanti del tipo di \_ Proprietà WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="6eb4b-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="6eb4b-104">Le costanti **di \_ \_ tipo di proprietà WINBIO** seguenti possono essere utilizzate per specificare l'origine delle informazioni sulle proprietà nella funzione [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .</span><span class="sxs-lookup"><span data-stu-id="6eb4b-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="6eb4b-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_sessione del \_ tipo di proprietà WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="6eb4b-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6eb4b-106">La proprietà si applica a una sessione biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="6eb4b-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb4b-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_modello di \_ tipo di proprietà WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="6eb4b-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6eb4b-108">La proprietà si applica a un modello biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="6eb4b-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb4b-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_unità del \_ tipo di proprietà WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="6eb4b-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6eb4b-110">La proprietà si applica a un'unità biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="6eb4b-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6eb4b-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_account del \_ tipo di proprietà WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="6eb4b-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6eb4b-112">La proprietà si applica a un account utente specifico che ha una registrazione biometrica.</span><span class="sxs-lookup"><span data-stu-id="6eb4b-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="6eb4b-113">Questo valore è supportato a partire da Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6eb4b-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6eb4b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6eb4b-114">Requirements</span></span>



| <span data-ttu-id="6eb4b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb4b-115">Requirement</span></span> | <span data-ttu-id="6eb4b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6eb4b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb4b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6eb4b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb4b-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6eb4b-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6eb4b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6eb4b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb4b-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6eb4b-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6eb4b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6eb4b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb4b-122"><dt>WinBio. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb4b-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb4b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6eb4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb4b-124">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="6eb4b-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="6eb4b-125">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="6eb4b-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





