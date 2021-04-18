---
title: Proprietà TargetName di ITsSbSession
description: Recupera il nome della destinazione in cui è stata creata la sessione.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetName
- Servizi Desktop remoto proprietà TargetName, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302604"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="5d7fc-106">Proprietà ITsSbSession:: TargetName</span><span class="sxs-lookup"><span data-stu-id="5d7fc-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="5d7fc-107">Recupera il nome della destinazione in cui è stata creata la sessione.</span><span class="sxs-lookup"><span data-stu-id="5d7fc-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="5d7fc-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5d7fc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7fc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d7fc-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="5d7fc-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5d7fc-110">Property value</span></span>

<span data-ttu-id="5d7fc-111">Puntatore a una variabile **BSTR** che riceve il nome della destinazione in cui è stata creata la sessione.</span><span class="sxs-lookup"><span data-stu-id="5d7fc-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7fc-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d7fc-112">Requirements</span></span>



| <span data-ttu-id="5d7fc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7fc-113">Requirement</span></span> | <span data-ttu-id="5d7fc-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5d7fc-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7fc-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d7fc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7fc-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5d7fc-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5d7fc-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d7fc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7fc-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d7fc-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="5d7fc-119">IDL</span><span class="sxs-lookup"><span data-stu-id="5d7fc-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d7fc-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d7fc-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7fc-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d7fc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7fc-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="5d7fc-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





