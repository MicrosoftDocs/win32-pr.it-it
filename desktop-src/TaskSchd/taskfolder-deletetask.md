---
title: TaskFolder. DeleteTask, metodo
description: Per lo scripting, Elimina un'attività dalla cartella.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Utilità di pianificazione del metodo DeleteTask
- Metodo DeleteTask Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, metodo DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742175"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="876e5-106">TaskFolder. DeleteTask, metodo</span><span class="sxs-lookup"><span data-stu-id="876e5-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="876e5-107">Per lo scripting, Elimina un'attività dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="876e5-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="876e5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="876e5-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="876e5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="876e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="876e5-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="876e5-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="876e5-111">Nome dell'attività specificata quando l'attività è stata registrata.</span><span class="sxs-lookup"><span data-stu-id="876e5-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="876e5-112">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="876e5-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="876e5-113">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="876e5-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="876e5-114">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="876e5-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="876e5-115">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="876e5-115">Not supported.</span></span> <span data-ttu-id="876e5-116">Il valore è 0</span><span class="sxs-lookup"><span data-stu-id="876e5-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="876e5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="876e5-117">Return value</span></span>

<span data-ttu-id="876e5-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="876e5-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="876e5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="876e5-119">Requirements</span></span>



| <span data-ttu-id="876e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="876e5-120">Requirement</span></span> | <span data-ttu-id="876e5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="876e5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="876e5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="876e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="876e5-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="876e5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="876e5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="876e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="876e5-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="876e5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="876e5-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="876e5-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="876e5-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="876e5-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="876e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="876e5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="876e5-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="876e5-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="876e5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="876e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876e5-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="876e5-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





