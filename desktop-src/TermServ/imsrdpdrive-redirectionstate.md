---
title: Proprietà RedirectionState di IMsRdpDrive
description: Indica lo stato di reindirizzamento dell'unità.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectionState
- Servizi Desktop remoto proprietà RedirectionState, interfaccia IMsRdpDrive
- Interfaccia IMsRdpDrive Servizi Desktop remoto, proprietà RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400787"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="db1de-106">Proprietà IMsRdpDrive:: RedirectionState</span><span class="sxs-lookup"><span data-stu-id="db1de-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="db1de-107">Indica lo stato di reindirizzamento dell'unità.</span><span class="sxs-lookup"><span data-stu-id="db1de-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="db1de-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="db1de-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="db1de-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db1de-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="db1de-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="db1de-110">Property value</span></span>

<span data-ttu-id="db1de-111">Impostare questo parametro su **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="db1de-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="db1de-112">per disabilitare il reindirizzamento o la **variante \_ true**.</span><span class="sxs-lookup"><span data-stu-id="db1de-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="db1de-113">per abilitare il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="db1de-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db1de-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="db1de-114">Error codes</span></span>

<span data-ttu-id="db1de-115">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="db1de-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="db1de-116">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="db1de-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="db1de-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db1de-117">Requirements</span></span>



| <span data-ttu-id="db1de-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db1de-118">Requirement</span></span> | <span data-ttu-id="db1de-119">Valore</span><span class="sxs-lookup"><span data-stu-id="db1de-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db1de-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db1de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db1de-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db1de-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="db1de-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db1de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db1de-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db1de-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="db1de-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="db1de-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="db1de-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db1de-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="db1de-126">DLL</span><span class="sxs-lookup"><span data-stu-id="db1de-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db1de-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db1de-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="db1de-128">IID</span><span class="sxs-lookup"><span data-stu-id="db1de-128">IID</span></span><br/>                      | <span data-ttu-id="db1de-129">IID \_ IMsRdpDrive è definito come d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="db1de-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="db1de-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db1de-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db1de-131">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="db1de-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





