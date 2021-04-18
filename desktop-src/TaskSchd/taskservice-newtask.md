---
title: TaskService. NewTask, metodo
description: Per lo scripting, restituisce un oggetto di definizione di attività vuoto da compilare con le impostazioni e le proprietà e quindi registrate usando il metodo TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Utilità di pianificazione del metodo NewTask
- Metodo NewTask Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo NewTask
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302670"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="17977-106">TaskService. NewTask, metodo</span><span class="sxs-lookup"><span data-stu-id="17977-106">TaskService.NewTask method</span></span>

<span data-ttu-id="17977-107">Per lo scripting, restituisce un oggetto di definizione di attività vuoto da compilare con le impostazioni e le proprietà e quindi registrate usando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="17977-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17977-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17977-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="17977-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="17977-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17977-110">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17977-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17977-111">Questo parametro è riservato per utilizzi futuri e deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="17977-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17977-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17977-112">Return value</span></span>

<span data-ttu-id="17977-113">Definizione di attività che specifica tutte le informazioni necessarie per creare una nuova attività.</span><span class="sxs-lookup"><span data-stu-id="17977-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="17977-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17977-114">Requirements</span></span>



| <span data-ttu-id="17977-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="17977-115">Requirement</span></span> | <span data-ttu-id="17977-116">Valore</span><span class="sxs-lookup"><span data-stu-id="17977-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17977-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17977-117">Minimum supported client</span></span><br/> | <span data-ttu-id="17977-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17977-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17977-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17977-119">Minimum supported server</span></span><br/> | <span data-ttu-id="17977-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17977-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17977-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="17977-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="17977-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17977-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17977-123">DLL</span><span class="sxs-lookup"><span data-stu-id="17977-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17977-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17977-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





