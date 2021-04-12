---
title: Proprietà Principal. RunLevel
description: Per gli script, ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Utilità di pianificazione proprietà RunLevel
- Utilità di pianificazione proprietà RunLevel, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517907"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="3df32-106">Proprietà Principal. RunLevel</span><span class="sxs-lookup"><span data-stu-id="3df32-106">Principal.RunLevel property</span></span>

<span data-ttu-id="3df32-107">Per gli script, ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3df32-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="3df32-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3df32-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df32-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3df32-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="3df32-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3df32-110">Property value</span></span>

<span data-ttu-id="3df32-111">Identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3df32-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="3df32-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3df32-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="3df32-113">Significato</span><span class="sxs-lookup"><span data-stu-id="3df32-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="3df32-114"><dt>**Attività \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3df32-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="3df32-115">Le attività verranno eseguite con i privilegi minimi (LUA).</span><span class="sxs-lookup"><span data-stu-id="3df32-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="3df32-116"><dt>**Attività \_ RUNLEVEL \_ più alto**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3df32-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3df32-117">Le attività verranno eseguite con i privilegi più elevati.</span><span class="sxs-lookup"><span data-stu-id="3df32-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="3df32-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3df32-118">Remarks</span></span>

<span data-ttu-id="3df32-119">Se un'attività viene registrata utilizzando l' \\ account Administrator predefinito o gli account del sistema locale o del servizio locale, la proprietà **runlevel** verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="3df32-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="3df32-120">Il valore della proprietà verrà ignorato anche se il controllo dell'account utente è disattivato.</span><span class="sxs-lookup"><span data-stu-id="3df32-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="3df32-121">Se un'attività viene registrata usando il gruppo Administrators per il contesto di sicurezza dell'attività, è necessario impostare anche la proprietà [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) su **attività \_ runlevel \_ più alta** se si vuole eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="3df32-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="3df32-122">Per ulteriori informazioni, vedere [contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3df32-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3df32-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3df32-123">Requirements</span></span>



| <span data-ttu-id="3df32-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df32-124">Requirement</span></span> | <span data-ttu-id="3df32-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3df32-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3df32-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3df32-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3df32-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3df32-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3df32-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3df32-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3df32-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3df32-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3df32-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3df32-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="3df32-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3df32-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3df32-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3df32-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df32-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df32-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df32-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3df32-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df32-135">**Principale**</span><span class="sxs-lookup"><span data-stu-id="3df32-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





