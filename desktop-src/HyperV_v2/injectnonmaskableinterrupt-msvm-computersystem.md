---
description: Inserisce un interrupt non mascherabile nella macchina virtuale.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Metodo Msvm_ComputerSystem:: InjectNonMaskableInterrupt'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306044"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a><span data-ttu-id="88116-103">\_Metodo MSVM ComputerSystem:: InjectNonMaskableInterrupt</span><span class="sxs-lookup"><span data-stu-id="88116-103">Msvm\_ComputerSystem::InjectNonMaskableInterrupt method</span></span>

<span data-ttu-id="88116-104">Inserisce un interrupt non mascherabile nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88116-104">Injects a non-maskable interrupt into the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="88116-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88116-105">Syntax</span></span>


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a><span data-ttu-id="88116-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88116-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88116-107">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="88116-107">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88116-108">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) per tenere traccia dello stato dell'inserimento di interrupt.</span><span class="sxs-lookup"><span data-stu-id="88116-108">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) to track the status of the interrupt injection.</span></span> <span data-ttu-id="88116-109">Questo riferimento può essere **null** se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="88116-109">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88116-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88116-110">Return value</span></span>

<span data-ttu-id="88116-111">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="88116-111">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="88116-112">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="88116-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="88116-113">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="88116-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="88116-114">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="88116-114">**Access Denied** (32769)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="88116-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88116-115">Requirements</span></span>



| <span data-ttu-id="88116-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88116-116">Requirement</span></span> | <span data-ttu-id="88116-117">Valore</span><span class="sxs-lookup"><span data-stu-id="88116-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88116-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88116-118">Minimum supported client</span></span><br/> | <span data-ttu-id="88116-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88116-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="88116-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88116-120">Minimum supported server</span></span><br/> | <span data-ttu-id="88116-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="88116-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88116-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88116-122">Namespace</span></span><br/>                | <span data-ttu-id="88116-123">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="88116-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="88116-124">MOF</span><span class="sxs-lookup"><span data-stu-id="88116-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88116-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88116-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88116-126">DLL</span><span class="sxs-lookup"><span data-stu-id="88116-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88116-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88116-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88116-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88116-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88116-129">**\_ComputerSystem MSVM**</span><span class="sxs-lookup"><span data-stu-id="88116-129">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

