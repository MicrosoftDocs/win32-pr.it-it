---
title: Proprietà di stato ITsSbSession
description: Recupera o specifica lo stato della sessione.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà stato
- Servizi Desktop remoto proprietà state, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà state
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb939a518ab1050d932349cd70c85bcd22edf3d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479102"
---
# <a name="itssbsessionstate-property"></a><span data-ttu-id="0b2a1-106">Proprietà ITsSbSession:: state</span><span class="sxs-lookup"><span data-stu-id="0b2a1-106">ITsSbSession::State property</span></span>

<span data-ttu-id="0b2a1-107">Recupera o specifica lo stato della sessione.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-107">Retrieves or specifies the session state.</span></span>

<span data-ttu-id="0b2a1-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2a1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b2a1-109">Syntax</span></span>


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a><span data-ttu-id="0b2a1-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0b2a1-110">Property value</span></span>

<span data-ttu-id="0b2a1-111">Valore dell'enumerazione di [**\_ stato TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) che indica lo stato di una sessione.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-111">A value of the [**TSSESSION\_STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) enumeration that indicates the state of a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b2a1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b2a1-112">Requirements</span></span>



| <span data-ttu-id="0b2a1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2a1-113">Requirement</span></span> | <span data-ttu-id="0b2a1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0b2a1-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2a1-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b2a1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2a1-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0b2a1-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="0b2a1-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b2a1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2a1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b2a1-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="0b2a1-119">IDL</span><span class="sxs-lookup"><span data-stu-id="0b2a1-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b2a1-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b2a1-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b2a1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b2a1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b2a1-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="0b2a1-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[<span data-ttu-id="0b2a1-123">**\_stato TSSESSION**</span><span class="sxs-lookup"><span data-stu-id="0b2a1-123">**TSSESSION\_STATE**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





