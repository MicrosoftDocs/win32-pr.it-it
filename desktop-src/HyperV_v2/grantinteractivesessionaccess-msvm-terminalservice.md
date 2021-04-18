---
description: Concede l'accesso alla sessione interattiva della macchina virtuale all'elenco specificato di trustee.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Metodo GrantInteractiveSessionAccess della classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310543"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="4193f-103">Metodo GrantInteractiveSessionAccess della classe MSVM \_ TerminalService</span><span class="sxs-lookup"><span data-stu-id="4193f-103">GrantInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="4193f-104">Concede l'accesso alla sessione interattiva della macchina virtuale all'elenco specificato di trustee.</span><span class="sxs-lookup"><span data-stu-id="4193f-104">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="4193f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4193f-105">Syntax</span></span>


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4193f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4193f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4193f-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4193f-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4193f-108">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale a cui verrà concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="4193f-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to which access will be granted.</span></span>

</dd> <dt>

<span data-ttu-id="4193f-109">*Trustee* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4193f-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4193f-110">Matrice di stringhe, ognuna delle quali identifica un trustee a cui viene concesso l'accesso alla sessione interattiva della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4193f-110">An array of strings, each identifying a trustee that will be granted access to the interactive session of the virtual machine.</span></span> <span data-ttu-id="4193f-111">Gli identificatori del trustee devono essere specificati nel formato compatibile con SAM Windows o nel formato stringa SID di Windows.</span><span class="sxs-lookup"><span data-stu-id="4193f-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="4193f-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4193f-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4193f-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4193f-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4193f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4193f-114">Return value</span></span>

<span data-ttu-id="4193f-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4193f-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4193f-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4193f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="4193f-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="4193f-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="4193f-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="4193f-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="4193f-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-122">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="4193f-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="4193f-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4193f-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4193f-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4193f-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4193f-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4193f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4193f-127">Requirements</span></span>



| <span data-ttu-id="4193f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4193f-128">Requirement</span></span> | <span data-ttu-id="4193f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4193f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4193f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4193f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4193f-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4193f-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4193f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4193f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4193f-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4193f-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4193f-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4193f-134">Namespace</span></span><br/>                | <span data-ttu-id="4193f-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4193f-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4193f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4193f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4193f-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4193f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4193f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4193f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4193f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4193f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4193f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4193f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4193f-141">**\_TerminalService MSVM**</span><span class="sxs-lookup"><span data-stu-id="4193f-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

