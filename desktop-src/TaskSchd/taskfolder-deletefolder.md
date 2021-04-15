---
title: TaskFolder. DeleteFolder, metodo
description: Per la creazione di script, Elimina una sottocartella dalla cartella padre.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Utilità di pianificazione del metodo DeleteFolder
- Metodo DeleteFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477482"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="35eda-106">TaskFolder. DeleteFolder, metodo</span><span class="sxs-lookup"><span data-stu-id="35eda-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="35eda-107">Per la creazione di script, Elimina una sottocartella dalla cartella padre.</span><span class="sxs-lookup"><span data-stu-id="35eda-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eda-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35eda-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="35eda-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35eda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35eda-110">*cartellaname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35eda-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35eda-111">Nome della sottocartella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="35eda-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="35eda-112">La cartella radice dell'attività è specificata con una barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="35eda-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="35eda-113">Questo parametro può essere un percorso relativo della cartella che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="35eda-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="35eda-114">Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="35eda-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="35eda-115">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="35eda-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="35eda-116">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="35eda-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="35eda-117">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35eda-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35eda-118">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="35eda-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35eda-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35eda-119">Return value</span></span>

<span data-ttu-id="35eda-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="35eda-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="35eda-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35eda-121">Requirements</span></span>



| <span data-ttu-id="35eda-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35eda-122">Requirement</span></span> | <span data-ttu-id="35eda-123">Valore</span><span class="sxs-lookup"><span data-stu-id="35eda-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35eda-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35eda-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35eda-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35eda-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35eda-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35eda-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35eda-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35eda-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35eda-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="35eda-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="35eda-129"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35eda-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35eda-130">DLL</span><span class="sxs-lookup"><span data-stu-id="35eda-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35eda-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35eda-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35eda-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35eda-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eda-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="35eda-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="35eda-134">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="35eda-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





