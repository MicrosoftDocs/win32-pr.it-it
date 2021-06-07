---
title: Metodo TaskFolder.CreateFolder
description: Per lo scripting, crea una cartella per le attività correlate.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Metodo CreateFolder Utilità di pianificazione
- Metodo CreateFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione , metodo CreateFolder
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
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387079"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="17a6e-106">Metodo TaskFolder.CreateFolder</span><span class="sxs-lookup"><span data-stu-id="17a6e-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="17a6e-107">Per lo scripting, crea una cartella per le attività correlate.</span><span class="sxs-lookup"><span data-stu-id="17a6e-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a6e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17a6e-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="17a6e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="17a6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a6e-110">*folderName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17a6e-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a6e-111">Nome utilizzato per identificare la cartella.</span><span class="sxs-lookup"><span data-stu-id="17a6e-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="17a6e-112">Se viene specificato \\ "FolderName SubFolder1 SubFolder2", verrà creato l'intero albero di cartelle se \\ le cartelle non esistono.</span><span class="sxs-lookup"><span data-stu-id="17a6e-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="17a6e-113">Questo parametro può essere un percorso relativo dell'istanza [**TaskFolder**](taskfolder.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="17a6e-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="17a6e-114">La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="17a6e-114">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="17a6e-115">Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="17a6e-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="17a6e-116">Il carattere '.' non può essere usato per specificare la cartella attività corrente e '..'</span><span class="sxs-lookup"><span data-stu-id="17a6e-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="17a6e-117">Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="17a6e-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="17a6e-118">*sddl* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="17a6e-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a6e-119">Descrittore di sicurezza associato alla cartella.</span><span class="sxs-lookup"><span data-stu-id="17a6e-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a6e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17a6e-120">Return value</span></span>

<span data-ttu-id="17a6e-121">Oggetto [**TaskFolder**](taskfolder.md) che rappresenta la nuova sottocartella.</span><span class="sxs-lookup"><span data-stu-id="17a6e-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a6e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17a6e-122">Requirements</span></span>



| <span data-ttu-id="17a6e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a6e-123">Requirement</span></span> | <span data-ttu-id="17a6e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="17a6e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a6e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17a6e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="17a6e-126">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17a6e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17a6e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17a6e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="17a6e-128">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="17a6e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17a6e-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="17a6e-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="17a6e-130"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17a6e-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17a6e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="17a6e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a6e-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a6e-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a6e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17a6e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a6e-134">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="17a6e-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





