---
title: Metodo TaskService. GetFolder
description: Per la creazione di script, ottiene una cartella di attività registrate.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Metodo GetFolder Utilità di pianificazione
- Metodo GetFolder Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo GetFolder
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
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302671"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="a1652-106">Metodo TaskService. GetFolder</span><span class="sxs-lookup"><span data-stu-id="a1652-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="a1652-107">Per la creazione di script, ottiene una cartella di attività registrate.</span><span class="sxs-lookup"><span data-stu-id="a1652-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1652-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1652-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="a1652-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1652-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1652-110">*percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1652-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1652-111">Percorso della cartella da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a1652-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="a1652-112">Non usare una barra rovesciata che segue il nome dell'ultima cartella nel percorso.</span><span class="sxs-lookup"><span data-stu-id="a1652-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="a1652-113">La cartella radice dell'attività è specificata con una barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="a1652-113">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="a1652-114">Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="a1652-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="a1652-115">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="a1652-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="a1652-116">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="a1652-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1652-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1652-117">Return value</span></span>

<span data-ttu-id="a1652-118">Oggetto [**TaskFolder**](taskfolder.md) per la cartella richiesta.</span><span class="sxs-lookup"><span data-stu-id="a1652-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1652-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1652-119">Requirements</span></span>



| <span data-ttu-id="a1652-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1652-120">Requirement</span></span> | <span data-ttu-id="a1652-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a1652-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1652-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1652-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1652-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1652-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a1652-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1652-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1652-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1652-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1652-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a1652-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1652-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1652-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1652-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a1652-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1652-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1652-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1652-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1652-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1652-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a1652-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





