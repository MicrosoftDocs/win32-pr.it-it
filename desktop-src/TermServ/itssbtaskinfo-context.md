---
title: Proprietà di contesto ITsSbTaskInfo
description: Recupera i byte del contesto associati all'attività.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà di contesto
- Servizi Desktop remoto di proprietà di contesto, interfaccia ITsSbTaskInfo
- Interfaccia ITsSbTaskInfo Servizi Desktop remoto, proprietà di contesto
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121374"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="b7356-106">Proprietà ITsSbTaskInfo:: context</span><span class="sxs-lookup"><span data-stu-id="b7356-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="b7356-107">Recupera i byte del contesto associati all'attività.</span><span class="sxs-lookup"><span data-stu-id="b7356-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="b7356-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b7356-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7356-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7356-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="b7356-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b7356-110">Property value</span></span>

<span data-ttu-id="b7356-111">Contesto dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b7356-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7356-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7356-112">Requirements</span></span>



| <span data-ttu-id="b7356-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7356-113">Requirement</span></span> | <span data-ttu-id="b7356-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b7356-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7356-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7356-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b7356-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b7356-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b7356-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7356-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b7356-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7356-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="b7356-119">IDL</span><span class="sxs-lookup"><span data-stu-id="b7356-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7356-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7356-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7356-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7356-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7356-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="b7356-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





