---
title: Oggetto ExecAction
description: Oggetto di scripting che rappresenta un'azione che esegue un'operazione della riga di comando.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Esegui Utilità di pianificazione azione, interfaccia
- Utilità di pianificazione oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121111"
---
# <a name="execaction-object"></a><span data-ttu-id="76f3e-106">Oggetto ExecAction</span><span class="sxs-lookup"><span data-stu-id="76f3e-106">ExecAction object</span></span>

<span data-ttu-id="76f3e-107">Oggetto di scripting che rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="76f3e-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="76f3e-108">Membri</span><span class="sxs-lookup"><span data-stu-id="76f3e-108">Members</span></span>

<span data-ttu-id="76f3e-109">L'oggetto **ExecAction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="76f3e-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="76f3e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76f3e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76f3e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76f3e-111">Properties</span></span>

<span data-ttu-id="76f3e-112">L'oggetto **ExecAction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="76f3e-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="76f3e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76f3e-113">Property</span></span>                                                            | <span data-ttu-id="76f3e-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="76f3e-114">Access type</span></span>           | <span data-ttu-id="76f3e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76f3e-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76f3e-116">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="76f3e-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="76f3e-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="76f3e-117">Read/write</span></span><br/> | <span data-ttu-id="76f3e-118">Ottiene o imposta gli argomenti associati all'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="76f3e-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="76f3e-119">**ID**</span><span class="sxs-lookup"><span data-stu-id="76f3e-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="76f3e-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="76f3e-120">Read/write</span></span><br/> | <span data-ttu-id="76f3e-121">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="76f3e-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="76f3e-122">Ottiene o imposta l'identificatore dell'azione.</span><span class="sxs-lookup"><span data-stu-id="76f3e-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="76f3e-123">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="76f3e-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="76f3e-124">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="76f3e-124">Read/write</span></span><br/> | <span data-ttu-id="76f3e-125">Ottiene o imposta il percorso di un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="76f3e-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="76f3e-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="76f3e-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="76f3e-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f3e-127">Read-only</span></span><br/>  | <span data-ttu-id="76f3e-128">Ereditato dall'oggetto [**azione**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="76f3e-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="76f3e-129">Ottiene il tipo dell'azione.</span><span class="sxs-lookup"><span data-stu-id="76f3e-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="76f3e-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="76f3e-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="76f3e-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="76f3e-131">Read/write</span></span><br/> | <span data-ttu-id="76f3e-132">Ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="76f3e-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76f3e-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="76f3e-133">Remarks</span></span>

<span data-ttu-id="76f3e-134">Se le variabili di ambiente vengono usate nelle proprietà [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)o [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , i valori delle variabili di ambiente vengono memorizzati nella cache e usati quando viene avviata la Taskeng.exe (il motore attività).</span><span class="sxs-lookup"><span data-stu-id="76f3e-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="76f3e-135">Le modifiche apportate alle variabili di ambiente che si verificano dopo l'avvio del motore attività non verranno usate dal motore delle attività.</span><span class="sxs-lookup"><span data-stu-id="76f3e-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="76f3e-136">Questa azione esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="76f3e-136">This action performs a command-line operation.</span></span> <span data-ttu-id="76f3e-137">Ad esempio, l'azione potrebbe eseguire uno script o avviare un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="76f3e-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="76f3e-138">Durante la lettura o la scrittura di codice XML, un'azione di esecuzione viene specificata nell'elemento [**Exec**](taskschedulerschema-exec-actiongroup-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="76f3e-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="76f3e-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="76f3e-139">Examples</span></span>

<span data-ttu-id="76f3e-140">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="76f3e-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76f3e-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76f3e-141">Requirements</span></span>



| <span data-ttu-id="76f3e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f3e-142">Requirement</span></span> | <span data-ttu-id="76f3e-143">Valore</span><span class="sxs-lookup"><span data-stu-id="76f3e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76f3e-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76f3e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="76f3e-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76f3e-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76f3e-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76f3e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="76f3e-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76f3e-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76f3e-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="76f3e-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="76f3e-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76f3e-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76f3e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="76f3e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76f3e-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76f3e-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





