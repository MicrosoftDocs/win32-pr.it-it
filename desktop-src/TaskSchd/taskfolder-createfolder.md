---
title: TaskFolder. CreateFolder, metodo
description: Per gli script, crea una cartella per le attività correlate.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Utilità di pianificazione del metodo CreateFolder
- Metodo CreateFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301910"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="76385-106">TaskFolder. CreateFolder, metodo</span><span class="sxs-lookup"><span data-stu-id="76385-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="76385-107">Per gli script, crea una cartella per le attività correlate.</span><span class="sxs-lookup"><span data-stu-id="76385-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="76385-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76385-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="76385-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="76385-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76385-110">*cartellaname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76385-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76385-111">Nome utilizzato per identificare la cartella.</span><span class="sxs-lookup"><span data-stu-id="76385-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="76385-112">Se si specifica "FolderName \\ Sottocartella1 \\ SubFolder2", verrà creato l'intero albero delle cartelle se le cartelle non esistono.</span><span class="sxs-lookup"><span data-stu-id="76385-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="76385-113">Questo parametro può essere un percorso relativo dell'istanza corrente di [**TaskFolder**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="76385-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="76385-114">La cartella radice dell'attività è specificata con una barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="76385-114">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="76385-115">Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="76385-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="76385-116">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="76385-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="76385-117">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="76385-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="76385-118">*SDDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76385-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76385-119">Descrittore di sicurezza associato alla cartella.</span><span class="sxs-lookup"><span data-stu-id="76385-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76385-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76385-120">Return value</span></span>

<span data-ttu-id="76385-121">Oggetto [**TaskFolder**](taskfolder.md) che rappresenta la nuova sottocartella.</span><span class="sxs-lookup"><span data-stu-id="76385-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="76385-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76385-122">Requirements</span></span>



| <span data-ttu-id="76385-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="76385-123">Requirement</span></span> | <span data-ttu-id="76385-124">Valore</span><span class="sxs-lookup"><span data-stu-id="76385-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76385-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76385-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76385-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76385-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76385-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76385-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76385-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76385-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76385-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="76385-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="76385-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76385-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76385-131">DLL</span><span class="sxs-lookup"><span data-stu-id="76385-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76385-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76385-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76385-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76385-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76385-134">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="76385-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





