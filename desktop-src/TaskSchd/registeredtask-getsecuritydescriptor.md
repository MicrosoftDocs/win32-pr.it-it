---
title: RegisteredTask. GetSecurityDescriptor, metodo
description: Per gli script, ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Utilità di pianificazione del metodo GetSecurityDescriptor
- Metodo GetSecurityDescriptor Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo GetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964680"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="c59e6-106">RegisteredTask. GetSecurityDescriptor, metodo</span><span class="sxs-lookup"><span data-stu-id="c59e6-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="c59e6-107">Per gli script, ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="c59e6-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59e6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c59e6-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="c59e6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c59e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c59e6-110">*securityInformation*</span><span class="sxs-lookup"><span data-stu-id="c59e6-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="c59e6-111">Informazioni di sicurezza da [**\_ informazioni di sicurezza**](/windows/desktop/SecAuthZ/security-information).</span><span class="sxs-lookup"><span data-stu-id="c59e6-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c59e6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c59e6-112">Return value</span></span>

<span data-ttu-id="c59e6-113">Descrittore di sicurezza per l'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="c59e6-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="c59e6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c59e6-114">Requirements</span></span>



| <span data-ttu-id="c59e6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c59e6-115">Requirement</span></span> | <span data-ttu-id="c59e6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c59e6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c59e6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c59e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c59e6-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c59e6-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c59e6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c59e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c59e6-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c59e6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c59e6-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c59e6-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c59e6-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c59e6-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c59e6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c59e6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c59e6-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c59e6-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59e6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c59e6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59e6-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="c59e6-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="c59e6-127">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c59e6-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="c59e6-128">**RegisteredTask. SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c59e6-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

