---
description: Recupera l'elenco di controllo di accesso discrezionale (DACL) corrente che controlla l'accesso alla sessione interattiva di una macchina virtuale.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Metodo GetInteractiveSessionACL della classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752234"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="84f63-103">Metodo GetInteractiveSessionACL della classe MSVM \_ TerminalService</span><span class="sxs-lookup"><span data-stu-id="84f63-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="84f63-104">Recupera l' *elenco di controllo di accesso discrezionale* (DACL) corrente che controlla l'accesso alla sessione interattiva di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84f63-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f63-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84f63-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="84f63-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84f63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f63-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84f63-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f63-108">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale di cui verrà recuperato il DACL.</span><span class="sxs-lookup"><span data-stu-id="84f63-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="84f63-109">*AccessControlList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="84f63-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84f63-110">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**\_ InteractiveSessionACE MSVM**](msvm-interactivesessionace.md) che rappresenta una *voce di controllo di accesso* (ACE) nell'elenco DACL della sessione interattiva della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84f63-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f63-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84f63-111">Return value</span></span>

<span data-ttu-id="84f63-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="84f63-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="84f63-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="84f63-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="84f63-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-115">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="84f63-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="84f63-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-117">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="84f63-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-118">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="84f63-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-119">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="84f63-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="84f63-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="84f63-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-122">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="84f63-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="84f63-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="84f63-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84f63-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84f63-124">Requirements</span></span>



| <span data-ttu-id="84f63-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f63-125">Requirement</span></span> | <span data-ttu-id="84f63-126">Valore</span><span class="sxs-lookup"><span data-stu-id="84f63-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f63-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f63-127">Minimum supported client</span></span><br/> | <span data-ttu-id="84f63-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="84f63-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84f63-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84f63-129">Minimum supported server</span></span><br/> | <span data-ttu-id="84f63-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="84f63-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84f63-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84f63-131">Namespace</span></span><br/>                | <span data-ttu-id="84f63-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84f63-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84f63-133">MOF</span><span class="sxs-lookup"><span data-stu-id="84f63-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f63-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f63-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f63-135">DLL</span><span class="sxs-lookup"><span data-stu-id="84f63-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f63-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84f63-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84f63-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84f63-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f63-138">**\_TerminalService MSVM**</span><span class="sxs-lookup"><span data-stu-id="84f63-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




