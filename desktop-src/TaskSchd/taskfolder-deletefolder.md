---
title: Metodo TaskFolder.DeleteFolder
description: Per lo scripting, elimina una sottocartella dalla cartella padre.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Metodo DeleteFolder Utilità di pianificazione
- Metodo DeleteFolder Utilità di pianificazione , oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione metodo , DeleteFolder
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
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387040"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="6074b-106">Metodo TaskFolder.DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="6074b-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="6074b-107">Per lo scripting, elimina una sottocartella dalla cartella padre.</span><span class="sxs-lookup"><span data-stu-id="6074b-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="6074b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6074b-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="6074b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6074b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6074b-110">*folderName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6074b-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6074b-111">Nome della sottocartella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6074b-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="6074b-112">La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="6074b-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="6074b-113">Questo parametro può essere un percorso relativo alla cartella che si vuole eliminare.</span><span class="sxs-lookup"><span data-stu-id="6074b-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="6074b-114">Un esempio di percorso di cartella di attività, nella cartella dell'attività radice, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="6074b-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="6074b-115">Il carattere '.' non può essere usato per specificare la cartella dell'attività corrente e '.'.</span><span class="sxs-lookup"><span data-stu-id="6074b-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="6074b-116">Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="6074b-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="6074b-117">*flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6074b-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6074b-118">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="6074b-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6074b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6074b-119">Return value</span></span>

<span data-ttu-id="6074b-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6074b-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6074b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6074b-121">Requirements</span></span>



| <span data-ttu-id="6074b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6074b-122">Requirement</span></span> | <span data-ttu-id="6074b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6074b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6074b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6074b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6074b-125">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="6074b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6074b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6074b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6074b-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6074b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6074b-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6074b-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="6074b-129"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6074b-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6074b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6074b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6074b-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6074b-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6074b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6074b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6074b-133">**Cartella attività**</span><span class="sxs-lookup"><span data-stu-id="6074b-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="6074b-134">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6074b-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





