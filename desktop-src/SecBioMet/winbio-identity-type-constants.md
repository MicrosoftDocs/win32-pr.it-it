---
title: Costanti WINBIO_IDENTITY_TYPE (tipi WinBio \_ . h)
description: Specificare il formato delle informazioni di identità contenute nella struttura di \_ identità WINBIO.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963993"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="4057d-103">Costanti del tipo di \_ identità WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="4057d-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="4057d-104">Le costanti **di \_ \_ tipo Identity WINBIO** seguenti possono essere utilizzate per specificare il formato delle informazioni di identità contenute nella struttura [**di \_ identità WINBIO**](winbio-identity.md) .</span><span class="sxs-lookup"><span data-stu-id="4057d-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="4057d-105">Costante</span><span class="sxs-lookup"><span data-stu-id="4057d-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="4057d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4057d-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="4057d-107"><dt>**\_tipo di ID WINBIO \_ \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="4057d-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="4057d-108">Al modello non è associato alcun ID.</span><span class="sxs-lookup"><span data-stu-id="4057d-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="4057d-109"><dt>**\_ \_ carattere jolly tipo ID WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4057d-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="4057d-110">La struttura corrisponde a tutte le identità del modello.</span><span class="sxs-lookup"><span data-stu-id="4057d-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="4057d-111"><dt>**\_ \_ GUID tipo ID \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="4057d-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="4057d-112">Un GUID identifica il modello.</span><span class="sxs-lookup"><span data-stu-id="4057d-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="4057d-113"><dt>**\_ \_ SID tipo ID \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="4057d-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="4057d-114">Un SID di account identifica il modello.</span><span class="sxs-lookup"><span data-stu-id="4057d-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="4057d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4057d-115">Requirements</span></span>



| <span data-ttu-id="4057d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4057d-116">Requirement</span></span> | <span data-ttu-id="4057d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4057d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4057d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4057d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4057d-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4057d-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4057d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4057d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4057d-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4057d-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4057d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4057d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4057d-123"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4057d-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4057d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4057d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4057d-125">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="4057d-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="4057d-126">**identità di WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="4057d-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





