---
title: Proprietà TaskFolder. GetSecurityDescriptor
description: Per la creazione di script, ottiene il descrittore di sicurezza per la cartella.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Utilità di pianificazione proprietà GetSecurityDescriptor
- Utilità di pianificazione proprietà GetSecurityDescriptor, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302173"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="a6dc7-106">Proprietà TaskFolder. GetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="a6dc7-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="a6dc7-107">Per la creazione di script, ottiene il descrittore di sicurezza per la cartella.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6dc7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6dc7-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="a6dc7-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a6dc7-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a6dc7-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6dc7-110">Requirements</span></span>



| <span data-ttu-id="a6dc7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6dc7-111">Requirement</span></span> | <span data-ttu-id="a6dc7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a6dc7-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6dc7-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6dc7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a6dc7-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6dc7-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a6dc7-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6dc7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a6dc7-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6dc7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6dc7-117">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6dc7-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6dc7-118"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a6dc7-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a6dc7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a6dc7-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6dc7-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6dc7-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6dc7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6dc7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6dc7-122">**TaskFolder. SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a6dc7-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="a6dc7-123">**RegisteredTask. SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a6dc7-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





