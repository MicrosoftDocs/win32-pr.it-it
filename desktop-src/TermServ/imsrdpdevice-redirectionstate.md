---
title: Proprietà RedirectionState di IMsRdpDevice
description: Indica lo stato del reindirizzamento del dispositivo.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectionState
- Servizi Desktop remoto proprietà RedirectionState, interfaccia IMsRdpDevice
- Interfaccia IMsRdpDevice Servizi Desktop remoto, proprietà RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476451"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="98197-106">Proprietà IMsRdpDevice:: RedirectionState</span><span class="sxs-lookup"><span data-stu-id="98197-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="98197-107">Indica lo stato del reindirizzamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98197-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="98197-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="98197-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98197-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98197-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="98197-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="98197-110">Property value</span></span>

<span data-ttu-id="98197-111">Impostare questo parametro su **Variant \_ false** per disabilitare il reindirizzamento o la **variante \_ true** per abilitare il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="98197-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="98197-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="98197-112">Error codes</span></span>

<span data-ttu-id="98197-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="98197-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="98197-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="98197-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="98197-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98197-115">Requirements</span></span>



| <span data-ttu-id="98197-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="98197-116">Requirement</span></span> | <span data-ttu-id="98197-117">Valore</span><span class="sxs-lookup"><span data-stu-id="98197-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98197-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98197-118">Minimum supported client</span></span><br/> | <span data-ttu-id="98197-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98197-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98197-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98197-120">Minimum supported server</span></span><br/> | <span data-ttu-id="98197-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98197-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98197-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="98197-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="98197-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98197-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98197-124">DLL</span><span class="sxs-lookup"><span data-stu-id="98197-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98197-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98197-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="98197-126">IID</span><span class="sxs-lookup"><span data-stu-id="98197-126">IID</span></span><br/>                      | <span data-ttu-id="98197-127">IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="98197-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="98197-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98197-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98197-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="98197-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





