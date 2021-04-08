---
title: Proprietà identificatore ITsSbTaskInfo
description: Recupera un GUID utilizzato come identificatore univoco da parte dell'agente attività.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà identificatore
- Servizi Desktop remoto proprietà identificatore, interfaccia ITsSbTaskInfo
- Interfaccia ITsSbTaskInfo Servizi Desktop remoto, proprietà Identifier
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743639"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="e4fb7-106">Proprietà ITsSbTaskInfo:: Identifier</span><span class="sxs-lookup"><span data-stu-id="e4fb7-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="e4fb7-107">Recupera un GUID utilizzato come identificatore univoco da parte dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="e4fb7-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="e4fb7-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e4fb7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fb7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4fb7-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="e4fb7-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e4fb7-110">Property value</span></span>

<span data-ttu-id="e4fb7-111">Puntatore a un valore **BSTR** che riceve il GUID.</span><span class="sxs-lookup"><span data-stu-id="e4fb7-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fb7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4fb7-112">Requirements</span></span>



| <span data-ttu-id="e4fb7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4fb7-113">Requirement</span></span> | <span data-ttu-id="e4fb7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e4fb7-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fb7-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4fb7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fb7-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e4fb7-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e4fb7-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4fb7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fb7-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4fb7-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e4fb7-119">IDL</span><span class="sxs-lookup"><span data-stu-id="e4fb7-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4fb7-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4fb7-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4fb7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4fb7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fb7-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="e4fb7-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





