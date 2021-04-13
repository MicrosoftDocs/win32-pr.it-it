---
title: Elemento RunLevel (runLevelType)
description: Contiene un valore che specifica il livello di contesto di sicurezza per l'esecuzione dell'attività.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Utilità di pianificazione elemento RunLevel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341303"
---
# <a name="runlevel-runleveltype-element"></a><span data-ttu-id="f6c2d-104">Elemento RunLevel (runLevelType)</span><span class="sxs-lookup"><span data-stu-id="f6c2d-104">RunLevel (runLevelType) Element</span></span>

<span data-ttu-id="f6c2d-105">Contiene un valore che specifica il livello di contesto di sicurezza per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-105">Contains a value that specifies the security context level for running the task.</span></span> <span data-ttu-id="f6c2d-106">È possibile specificare di eseguire un'attività usando privilegi minimi o privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-106">You can specify to run a task using least privileges or elevated privileges.</span></span> <span data-ttu-id="f6c2d-107">Il valore 0 specifica che per eseguire l'attività con privilegi più bassi e il valore 1 viene specificato di eseguire l'attività con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-107">A value of 0 specifies to run the task with lowest privileges, and a value of 1 specifies to run the task with elevated privileges.</span></span>

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

<span data-ttu-id="f6c2d-108">L'elemento **runlevel** è definito dal tipo semplice [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c2d-108">The **RunLevel** element is defined by the [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f6c2d-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f6c2d-109">Parent element</span></span>



| <span data-ttu-id="f6c2d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6c2d-110">Element</span></span>                                                                                  | <span data-ttu-id="f6c2d-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="f6c2d-111">Derived from</span></span>                                                           | <span data-ttu-id="f6c2d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6c2d-112">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6c2d-113">**Entità (principalType)**</span><span class="sxs-lookup"><span data-stu-id="f6c2d-113">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="f6c2d-114">**principalType**</span><span class="sxs-lookup"><span data-stu-id="f6c2d-114">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="f6c2d-115">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-115">Specifies the security credentials for a principal.</span></span> <span data-ttu-id="f6c2d-116">Queste credenziali definiscono il contesto di sicurezza in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-116">These credentials define the security context that a task runs under.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="f6c2d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6c2d-117">Remarks</span></span>

<span data-ttu-id="f6c2d-118">Per lo sviluppo in C++, vedere [**Proprietà runlevel di IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span><span class="sxs-lookup"><span data-stu-id="f6c2d-118">For C++ development, see [**RunLevel Property of IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).</span></span>

<span data-ttu-id="f6c2d-119">Per lo sviluppo di script, vedere [**Principal. runlevel**](principal-runlevel.md).</span><span class="sxs-lookup"><span data-stu-id="f6c2d-119">For script development, see [**Principal.RunLevel**](principal-runlevel.md).</span></span>

<span data-ttu-id="f6c2d-120">Se un'attività viene registrata con l'account **\\ Administrator predefinito** o con gli account [LocalSystem](/windows/desktop/Services/localsystem-account) o [LocalService](/windows/desktop/Services/localservice-account) , la proprietà [**runlevel**](principal-runlevel.md) viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-120">If a task is registered using the **Builtin\\Administrator** account or the [LocalSystem](/windows/desktop/Services/localsystem-account) or [LocalService](/windows/desktop/Services/localservice-account) accounts, the [**RunLevel**](principal-runlevel.md) property is ignored.</span></span> <span data-ttu-id="f6c2d-121">Il valore dell'attributo verrà ignorato anche se il [controllo dell'account utente](/windows/desktop/SecAuthZ/user-account-control) è disattivato.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-121">The attribute value will also be ignored if [User Account Control](/windows/desktop/SecAuthZ/user-account-control) (UAC) is turned off.</span></span>

<span data-ttu-id="f6c2d-122">Se un'attività viene registrata usando il gruppo **Administrators** per il contesto di sicurezza dell'attività, è necessario impostare anche la proprietà [**runlevel**](principal-runlevel.md) su "highestAvailable" per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-122">If a task is registered using the **Administrators** group for the security context of the task, then you must also set the [**RunLevel**](principal-runlevel.md) property to "HighestAvailable" to run the task.</span></span> <span data-ttu-id="f6c2d-123">Per ulteriori informazioni, vedere [contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="f6c2d-123">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c2d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6c2d-124">Requirements</span></span>



| <span data-ttu-id="f6c2d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6c2d-125">Requirement</span></span> | <span data-ttu-id="f6c2d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f6c2d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6c2d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6c2d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c2d-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6c2d-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6c2d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6c2d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c2d-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6c2d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

