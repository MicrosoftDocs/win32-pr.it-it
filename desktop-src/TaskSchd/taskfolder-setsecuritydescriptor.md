---
title: Proprietà TaskFolder. SetSecurityDescriptor
description: Per lo scripting, imposta il descrittore di sicurezza per la cartella.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Utilità di pianificazione proprietà SetSecurityDescriptor
- Utilità di pianificazione proprietà SetSecurityDescriptor, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963987"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="0a4db-106">Proprietà TaskFolder. SetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="0a4db-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="0a4db-107">Per lo scripting, imposta il descrittore di sicurezza per la cartella.</span><span class="sxs-lookup"><span data-stu-id="0a4db-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4db-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a4db-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="0a4db-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0a4db-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4db-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a4db-110">Remarks</span></span>

<span data-ttu-id="0a4db-111">È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per una cartella attività per consentire o negare a determinati utenti e gruppi l'accesso a una cartella attività.</span><span class="sxs-lookup"><span data-stu-id="0a4db-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4db-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a4db-112">Requirements</span></span>



| <span data-ttu-id="0a4db-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4db-113">Requirement</span></span> | <span data-ttu-id="0a4db-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0a4db-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4db-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a4db-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4db-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a4db-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0a4db-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a4db-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4db-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a4db-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a4db-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a4db-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a4db-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a4db-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a4db-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0a4db-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a4db-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a4db-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a4db-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a4db-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4db-124">**RegisteredTask. SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0a4db-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="0a4db-125">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0a4db-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





