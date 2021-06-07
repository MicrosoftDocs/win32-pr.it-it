---
title: Metodo TaskService.GetFolder
description: Per lo scripting, ottiene una cartella di attività registrate.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Metodo GetFolder Utilità di pianificazione
- Metodo GetFolder Utilità di pianificazione , oggetto TaskService
- Oggetto TaskService Utilità di pianificazione metodo , GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387100"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="5e7ae-106">Metodo TaskService.GetFolder</span><span class="sxs-lookup"><span data-stu-id="5e7ae-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="5e7ae-107">Per lo scripting, ottiene una cartella di attività registrate.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e7ae-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="5e7ae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e7ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e7ae-110">*path* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e7ae-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7ae-111">Percorso della cartella da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="5e7ae-112">Non usare una barra rovesciata dopo l'ultimo nome di cartella nel percorso.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="5e7ae-113">La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="5e7ae-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="5e7ae-114">Un esempio di percorso di cartella di attività, nella cartella dell'attività radice, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="5e7ae-115">Il carattere '.' non può essere usato per specificare la cartella dell'attività corrente e '.'.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="5e7ae-116">Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e7ae-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e7ae-117">Return value</span></span>

<span data-ttu-id="5e7ae-118">Oggetto [**TaskFolder**](taskfolder.md) per la cartella richiesta.</span><span class="sxs-lookup"><span data-stu-id="5e7ae-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7ae-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e7ae-119">Requirements</span></span>



| <span data-ttu-id="5e7ae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7ae-120">Requirement</span></span> | <span data-ttu-id="5e7ae-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5e7ae-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7ae-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e7ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e7ae-123">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e7ae-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5e7ae-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e7ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e7ae-125">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e7ae-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e7ae-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5e7ae-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e7ae-127"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e7ae-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e7ae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5e7ae-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e7ae-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e7ae-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e7ae-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e7ae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7ae-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5e7ae-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





