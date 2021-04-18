---
title: Proprietà RunningTask. EnginePID
description: Per gli script, ottiene l'ID processo per il motore (processo) che esegue l'attività.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Utilità di pianificazione proprietà EnginePID
- Utilità di pianificazione proprietà EnginePID, oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione, proprietà EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301911"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="4151f-106">Proprietà RunningTask. EnginePID</span><span class="sxs-lookup"><span data-stu-id="4151f-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="4151f-107">Per gli script, ottiene l'ID processo per il motore (processo) che esegue l'attività.</span><span class="sxs-lookup"><span data-stu-id="4151f-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="4151f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4151f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4151f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4151f-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="4151f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4151f-110">Property value</span></span>

<span data-ttu-id="4151f-111">ID del processo per il motore che esegue l'attività.</span><span class="sxs-lookup"><span data-stu-id="4151f-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="4151f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4151f-112">Remarks</span></span>

<span data-ttu-id="4151f-113">L'ID di processo restituito da questa proprietà non può essere aggiunto direttamente a una stringa.</span><span class="sxs-lookup"><span data-stu-id="4151f-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="4151f-114">Il valore restituito deve essere convertito in un valore integer prima chiamando la funzione [CInt](/previous-versions//fctcwhw9(v=vs.85)) sul valore restituito.</span><span class="sxs-lookup"><span data-stu-id="4151f-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="4151f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4151f-115">Requirements</span></span>



| <span data-ttu-id="4151f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4151f-116">Requirement</span></span> | <span data-ttu-id="4151f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4151f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4151f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4151f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4151f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4151f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4151f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4151f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4151f-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4151f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4151f-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4151f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4151f-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4151f-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4151f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4151f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4151f-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4151f-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

