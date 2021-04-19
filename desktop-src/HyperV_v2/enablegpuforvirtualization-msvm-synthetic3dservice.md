---
description: Abilita una GPU fisica per la virtualizzazione.
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: Metodo EnableGPUForVirtualization della classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.EnableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cf21424e9af8398cd435dce409bccde03543a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315502"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="c1dfe-103">Metodo EnableGPUForVirtualization della classe MSVM \_ Synthetic3DService</span><span class="sxs-lookup"><span data-stu-id="c1dfe-103">EnableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="c1dfe-104">Abilita una GPU fisica per la virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-104">Enables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dfe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1dfe-105">Syntax</span></span>


```mof
uint32 EnableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c1dfe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1dfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1dfe-107">*PhysicalGPU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1dfe-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfe-108">Riferimento a un'istanza della classe [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) che rappresenta la GPU fisica da abilitare.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="c1dfe-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c1dfe-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dfe-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c1dfe-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1dfe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1dfe-111">Return value</span></span>

<span data-ttu-id="c1dfe-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1dfe-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c1dfe-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c1dfe-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1dfe-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="c1dfe-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c1dfe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1dfe-115">Requirements</span></span>



| <span data-ttu-id="c1dfe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1dfe-116">Requirement</span></span> | <span data-ttu-id="c1dfe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c1dfe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dfe-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1dfe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1dfe-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c1dfe-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1dfe-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1dfe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1dfe-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c1dfe-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1dfe-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1dfe-122">Namespace</span></span><br/>                | <span data-ttu-id="c1dfe-123">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1dfe-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1dfe-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c1dfe-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1dfe-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1dfe-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1dfe-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c1dfe-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1dfe-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1dfe-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1dfe-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1dfe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1dfe-129">**\_Synthetic3DService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c1dfe-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

