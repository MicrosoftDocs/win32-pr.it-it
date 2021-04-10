---
title: Costanti WINBIO_BIR_QUALITY (tipi WinBio \_ . h)
description: Specificare la qualità relativa dei dati biometrici in BIR se non è stato specificato un valore intero compreso tra 0 e 100.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121446"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="5f84f-103">\_Costanti di \_ qualità WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="5f84f-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="5f84f-104">I flag seguenti vengono usati dal membro **dataquality** della struttura dell' [**\_ \_ intestazione WINBIO bir**](winbio-bir-header.md) per specificare la qualità relativa dei dati biometrici in Bir se non è stato specificato un valore intero compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="5f84f-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="5f84f-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="5f84f-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="5f84f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f84f-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="5f84f-107"><dt>**WINBIO \_ DATA \_ Quality \_ non \_ impostata**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="5f84f-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="5f84f-108">Le misurazioni di qualità sono supportate dal creatore di BIR, ma in BIR non è impostato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="5f84f-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="5f84f-109"><dt>**WINBIO \_ DATA \_ Quality \_ non \_ supportata**</dt> <dt> 2</dt></span><span class="sxs-lookup"><span data-stu-id="5f84f-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="5f84f-110">Le misurazioni di qualità non sono supportate da BIR Creator.</span><span class="sxs-lookup"><span data-stu-id="5f84f-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="5f84f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f84f-111">Requirements</span></span>



| <span data-ttu-id="5f84f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f84f-112">Requirement</span></span> | <span data-ttu-id="5f84f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5f84f-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f84f-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f84f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5f84f-115">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5f84f-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5f84f-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f84f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5f84f-117">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f84f-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5f84f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f84f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f84f-119"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f84f-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f84f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f84f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f84f-121">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="5f84f-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





