---
description: Revoca l'accesso alla sessione interattiva della macchina virtuale dall'elenco specificato di trustee.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Metodo RevokeInteractiveSessionAccess della classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756500"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="f59b2-103">Metodo RevokeInteractiveSessionAccess della classe MSVM \_ TerminalService</span><span class="sxs-lookup"><span data-stu-id="f59b2-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="f59b2-104">Revoca l'accesso alla sessione interattiva della macchina virtuale dall'elenco specificato di trustee.</span><span class="sxs-lookup"><span data-stu-id="f59b2-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="f59b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f59b2-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f59b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f59b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f59b2-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f59b2-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f59b2-108">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta la macchina virtuale a cui verrà revocato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="f59b2-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="f59b2-109">*Trustee* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f59b2-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f59b2-110">Matrice di stringhe, ognuna delle quali identifica un trustee i cui diritti di accesso verranno revocati.</span><span class="sxs-lookup"><span data-stu-id="f59b2-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="f59b2-111">Gli identificatori del trustee devono essere specificati nel formato compatibile con SAM Windows o nel formato stringa SID di Windows.</span><span class="sxs-lookup"><span data-stu-id="f59b2-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="f59b2-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f59b2-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f59b2-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f59b2-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f59b2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f59b2-114">Return value</span></span>

<span data-ttu-id="f59b2-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f59b2-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f59b2-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="f59b2-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f59b2-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="f59b2-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="f59b2-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="f59b2-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="f59b2-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-122">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="f59b2-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f59b2-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="f59b2-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f59b2-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f59b2-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f59b2-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f59b2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f59b2-127">Requirements</span></span>



| <span data-ttu-id="f59b2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f59b2-128">Requirement</span></span> | <span data-ttu-id="f59b2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f59b2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f59b2-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f59b2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f59b2-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f59b2-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f59b2-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f59b2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f59b2-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f59b2-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f59b2-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f59b2-134">Namespace</span></span><br/>                | <span data-ttu-id="f59b2-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f59b2-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f59b2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f59b2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f59b2-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f59b2-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f59b2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f59b2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f59b2-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f59b2-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f59b2-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f59b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59b2-141">**\_TerminalService MSVM**</span><span class="sxs-lookup"><span data-stu-id="f59b2-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

