---
title: RegisteredTask. SetSecurityDescriptor, metodo
description: Per lo scripting, imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Utilità di pianificazione del metodo SetSecurityDescriptor
- Metodo SetSecurityDescriptor Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121107"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="8c82d-106">RegisteredTask. SetSecurityDescriptor, metodo</span><span class="sxs-lookup"><span data-stu-id="8c82d-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="8c82d-107">Per lo scripting, imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="8c82d-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c82d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c82d-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="8c82d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c82d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c82d-110">*SDDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c82d-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c82d-111">Descrittore di sicurezza utilizzato come credenziali per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="8c82d-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="8c82d-112">Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="8c82d-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c82d-113">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c82d-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c82d-114">Flag che specificano come impostare il descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8c82d-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="8c82d-115">\_ \_ È possibile specificare l'attività non aggiungere il \_ \_ flag ACE principale (0x10) dell'enumerazione per la [**\_ creazione di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="8c82d-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c82d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c82d-116">Return value</span></span>

<span data-ttu-id="8c82d-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8c82d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c82d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c82d-118">Remarks</span></span>

<span data-ttu-id="8c82d-119">È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.</span><span class="sxs-lookup"><span data-stu-id="8c82d-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c82d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c82d-120">Requirements</span></span>



| <span data-ttu-id="8c82d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c82d-121">Requirement</span></span> | <span data-ttu-id="8c82d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8c82d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c82d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c82d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c82d-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c82d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8c82d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c82d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c82d-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c82d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c82d-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8c82d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c82d-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8c82d-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8c82d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8c82d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c82d-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c82d-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c82d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c82d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c82d-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="8c82d-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="8c82d-133">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8c82d-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="8c82d-134">**RegisteredTask. SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8c82d-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





