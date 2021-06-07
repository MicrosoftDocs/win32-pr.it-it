---
title: TaskFolder.GetTask - proprietà
description: Per lo scripting, ottiene un'attività in un percorso specificato in una cartella.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Proprietà GetTask Utilità di pianificazione
- Proprietà GetTask Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione proprietà , GetTask
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387677"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="d4123-106">TaskFolder.GetTask - proprietà</span><span class="sxs-lookup"><span data-stu-id="d4123-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="d4123-107">Per lo scripting, ottiene un'attività in un percorso specificato in una cartella.</span><span class="sxs-lookup"><span data-stu-id="d4123-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4123-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4123-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="d4123-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d4123-109">Property value</span></span>

<span data-ttu-id="d4123-110">Percorso (percorso) dell'attività in una cartella.</span><span class="sxs-lookup"><span data-stu-id="d4123-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="d4123-111">La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="d4123-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="d4123-112">Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="d4123-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="d4123-113">Il carattere '.' non può essere usato per specificare la cartella attività corrente e '..'</span><span class="sxs-lookup"><span data-stu-id="d4123-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="d4123-114">Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="d4123-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4123-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d4123-115">Error codes</span></span>

<span data-ttu-id="d4123-116">Attività nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="d4123-116">The task at the specified location.</span></span> <span data-ttu-id="d4123-117">L'attività è un [**oggetto RegisteredTask.**](registeredtask.md)</span><span class="sxs-lookup"><span data-stu-id="d4123-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4123-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4123-118">Requirements</span></span>



| <span data-ttu-id="d4123-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4123-119">Requirement</span></span> | <span data-ttu-id="d4123-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d4123-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4123-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4123-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d4123-122">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d4123-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d4123-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4123-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d4123-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4123-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4123-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d4123-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4123-126"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4123-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4123-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d4123-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4123-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4123-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





