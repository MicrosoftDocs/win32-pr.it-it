---
title: Proprietà stato ITsSbTaskInfo
description: Recupera un \_ \_ valore di enumerazione dello stato dell'attività RDV che rappresenta lo stato dell'attività.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Proprietà Status Servizi Desktop remoto
- Servizi Desktop remoto proprietà stato, interfaccia ITsSbTaskInfo
- Interfaccia ITsSbTaskInfo Servizi Desktop remoto, proprietà Status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741311"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="a27b4-106">Proprietà ITsSbTaskInfo:: status</span><span class="sxs-lookup"><span data-stu-id="a27b4-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="a27b4-107">Recupera un valore di enumerazione [**\_ \_ dello stato dell'attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a27b4-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="a27b4-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a27b4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a27b4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a27b4-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="a27b4-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a27b4-110">Property value</span></span>

<span data-ttu-id="a27b4-111">Valore di enumerazione [**\_ \_ dello stato dell'attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a27b4-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="a27b4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a27b4-112">Requirements</span></span>



| <span data-ttu-id="a27b4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a27b4-113">Requirement</span></span> | <span data-ttu-id="a27b4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a27b4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a27b4-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a27b4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a27b4-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a27b4-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="a27b4-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a27b4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a27b4-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a27b4-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a27b4-119">IDL</span><span class="sxs-lookup"><span data-stu-id="a27b4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a27b4-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a27b4-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a27b4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a27b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a27b4-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="a27b4-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





