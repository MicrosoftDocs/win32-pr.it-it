---
title: Proprietà TaskFolder. GetTask
description: Per gli script, ottiene un'attività in una posizione specificata in una cartella.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Utilità di pianificazione proprietà GetTask
- Utilità di pianificazione proprietà GetTask, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà GetTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740599"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="bd6a2-106">Proprietà TaskFolder. GetTask</span><span class="sxs-lookup"><span data-stu-id="bd6a2-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="bd6a2-107">Per gli script, ottiene un'attività in una posizione specificata in una cartella.</span><span class="sxs-lookup"><span data-stu-id="bd6a2-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6a2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd6a2-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="bd6a2-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bd6a2-109">Property value</span></span>

<span data-ttu-id="bd6a2-110">Percorso (percorso) dell'attività in una cartella.</span><span class="sxs-lookup"><span data-stu-id="bd6a2-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="bd6a2-111">La cartella radice dell'attività è specificata con una barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="bd6a2-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="bd6a2-112">Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="bd6a2-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="bd6a2-113">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="bd6a2-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="bd6a2-114">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="bd6a2-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd6a2-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bd6a2-115">Error codes</span></span>

<span data-ttu-id="bd6a2-116">Attività nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="bd6a2-116">The task at the specified location.</span></span> <span data-ttu-id="bd6a2-117">L'attività è un oggetto [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="bd6a2-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6a2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd6a2-118">Requirements</span></span>



| <span data-ttu-id="bd6a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6a2-119">Requirement</span></span> | <span data-ttu-id="bd6a2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bd6a2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6a2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd6a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6a2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd6a2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bd6a2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd6a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6a2-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd6a2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd6a2-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bd6a2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd6a2-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd6a2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd6a2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bd6a2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd6a2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd6a2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





