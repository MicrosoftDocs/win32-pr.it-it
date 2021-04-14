---
description: Disabilita una GPU fisica per la virtualizzazione.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Metodo DisableGPUForVirtualization della classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2634a3196e0c59368002151426e6f1407a13db8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342636"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="bb583-103">Metodo DisableGPUForVirtualization della classe MSVM \_ Synthetic3DService</span><span class="sxs-lookup"><span data-stu-id="bb583-103">DisableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="bb583-104">Disabilita una GPU fisica per la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bb583-104">Disables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb583-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb583-105">Syntax</span></span>


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bb583-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb583-107">*PhysicalGPU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb583-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb583-108">Riferimento a un'istanza della classe [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) che rappresenta la GPU fisica da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="bb583-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="bb583-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="bb583-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb583-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb583-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb583-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb583-111">Return value</span></span>

<span data-ttu-id="bb583-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb583-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bb583-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="bb583-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bb583-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="bb583-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bb583-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb583-115">Requirements</span></span>



| <span data-ttu-id="bb583-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb583-116">Requirement</span></span> | <span data-ttu-id="bb583-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bb583-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb583-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb583-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb583-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bb583-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb583-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb583-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb583-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb583-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb583-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb583-122">Namespace</span></span><br/>                | <span data-ttu-id="bb583-123">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb583-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb583-124">MOF</span><span class="sxs-lookup"><span data-stu-id="bb583-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb583-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb583-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb583-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bb583-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb583-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb583-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb583-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb583-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb583-129">**\_Synthetic3DService MSVM**</span><span class="sxs-lookup"><span data-stu-id="bb583-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

