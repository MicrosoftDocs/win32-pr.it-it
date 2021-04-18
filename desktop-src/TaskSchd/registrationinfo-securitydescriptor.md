---
title: Proprietà RegistrationInfo. SecurityDescriptor
description: Per lo scripting, ottiene o imposta il descrittore di sicurezza dell'attività.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Utilità di pianificazione proprietà SecurityDescriptor
- Utilità di pianificazione proprietà SecurityDescriptor, oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione, proprietà SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300938"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="7a1c9-106">Proprietà RegistrationInfo. SecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="7a1c9-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="7a1c9-107">Per lo scripting, ottiene o imposta il descrittore di sicurezza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7a1c9-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="7a1c9-108">Se durante la registrazione dell'attività viene fornito un descrittore di sicurezza diverso, il descrittore di sicurezza impostato con questa proprietà verrà sostituito.</span><span class="sxs-lookup"><span data-stu-id="7a1c9-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a1c9-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="7a1c9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7a1c9-110">Property value</span></span>

<span data-ttu-id="7a1c9-111">Descrittore di sicurezza associato all'attività.</span><span class="sxs-lookup"><span data-stu-id="7a1c9-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a1c9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a1c9-112">Remarks</span></span>

<span data-ttu-id="7a1c9-113">Durante la lettura o la scrittura di codice XML per un'attività, il descrittore di sicurezza dell'attività viene specificato utilizzando l'elemento [**securityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7a1c9-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a1c9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a1c9-114">Requirements</span></span>



| <span data-ttu-id="7a1c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a1c9-115">Requirement</span></span> | <span data-ttu-id="7a1c9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7a1c9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1c9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a1c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1c9-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a1c9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7a1c9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a1c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1c9-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a1c9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a1c9-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7a1c9-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a1c9-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a1c9-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a1c9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7a1c9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a1c9-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a1c9-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a1c9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a1c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1c9-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7a1c9-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





