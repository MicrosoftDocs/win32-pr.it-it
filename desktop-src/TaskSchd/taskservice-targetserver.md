---
title: Proprietà TaskService. TargetServer
description: Per gli script, ottiene il nome del computer in cui è in esecuzione il Utilità di pianificazione servizio a cui è connesso l'utente.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Utilità di pianificazione proprietà TargetServer
- Utilità di pianificazione proprietà TargetServer, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, proprietà TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519094"
---
# <a name="taskservicetargetserver-property"></a><span data-ttu-id="82349-106">Proprietà TaskService. TargetServer</span><span class="sxs-lookup"><span data-stu-id="82349-106">TaskService.TargetServer property</span></span>

<span data-ttu-id="82349-107">Per gli script, ottiene il nome del computer in cui è in esecuzione il Utilità di pianificazione servizio a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="82349-107">For scripting, gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="syntax"></a><span data-ttu-id="82349-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82349-108">Syntax</span></span>


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a><span data-ttu-id="82349-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="82349-109">Property value</span></span>

<span data-ttu-id="82349-110">Nome del computer che esegue il servizio Utilità di pianificazione a cui è connesso l'utente.</span><span class="sxs-lookup"><span data-stu-id="82349-110">The name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="remarks"></a><span data-ttu-id="82349-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="82349-111">Remarks</span></span>

<span data-ttu-id="82349-112">Questa proprietà restituisce una stringa vuota quando l'utente passa un indirizzo IP, localhost o ' .' come parametro e restituisce il nome del computer che esegue il servizio Utilità di pianificazione quando l'utente non passa alcun valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="82349-112">This property returns an empty string when the user passes an IP address, Localhost, or '.' as a parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.</span></span>

## <a name="requirements"></a><span data-ttu-id="82349-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82349-113">Requirements</span></span>



| <span data-ttu-id="82349-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82349-114">Requirement</span></span> | <span data-ttu-id="82349-115">Valore</span><span class="sxs-lookup"><span data-stu-id="82349-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82349-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82349-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82349-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82349-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="82349-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82349-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82349-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82349-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82349-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="82349-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="82349-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82349-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82349-122">DLL</span><span class="sxs-lookup"><span data-stu-id="82349-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82349-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82349-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





