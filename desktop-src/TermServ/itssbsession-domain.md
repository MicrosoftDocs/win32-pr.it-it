---
title: Proprietà di dominio ITsSbSession
description: Recupera il nome di dominio dell'utente.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà di dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà del dominio
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302606"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="edb1f-106">ITsSbSession::D Proprietà ominio</span><span class="sxs-lookup"><span data-stu-id="edb1f-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="edb1f-107">Recupera il nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="edb1f-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="edb1f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="edb1f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb1f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edb1f-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="edb1f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="edb1f-110">Property value</span></span>

<span data-ttu-id="edb1f-111">Puntatore a una variabile **BSTR** che riceve il nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="edb1f-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb1f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edb1f-112">Requirements</span></span>



| <span data-ttu-id="edb1f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb1f-113">Requirement</span></span> | <span data-ttu-id="edb1f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="edb1f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="edb1f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edb1f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="edb1f-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="edb1f-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="edb1f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edb1f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="edb1f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edb1f-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="edb1f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="edb1f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edb1f-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="edb1f-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb1f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edb1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb1f-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="edb1f-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





