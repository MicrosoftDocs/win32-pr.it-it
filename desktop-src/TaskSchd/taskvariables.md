---
title: Oggetto TaskVariables
description: Oggetto di script che definisce le variabili dell'attività che possono essere passate come parametri ai gestori di attività e ai file eseguibili esterni avviati dalle attività.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Utilità di pianificazione oggetto TaskVariables
- Oggetto TaskVariables Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478352"
---
# <a name="taskvariables-object"></a><span data-ttu-id="3810e-105">Oggetto TaskVariables</span><span class="sxs-lookup"><span data-stu-id="3810e-105">TaskVariables object</span></span>

<span data-ttu-id="3810e-106">Oggetto di script che definisce le variabili dell'attività che possono essere passate come parametri ai gestori di attività e ai file eseguibili esterni avviati dalle attività.</span><span class="sxs-lookup"><span data-stu-id="3810e-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="3810e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="3810e-107">Members</span></span>

<span data-ttu-id="3810e-108">L'oggetto **TaskVariables** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3810e-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="3810e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="3810e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3810e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="3810e-110">Methods</span></span>

<span data-ttu-id="3810e-111">L'oggetto **TaskVariables** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3810e-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="3810e-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="3810e-112">Method</span></span>                                         | <span data-ttu-id="3810e-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3810e-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3810e-114">**GetContext**</span><span class="sxs-lookup"><span data-stu-id="3810e-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="3810e-115">Utilizzato per condividere il contesto tra diversi passaggi e attività che si trovano nella stessa istanza del processo.</span><span class="sxs-lookup"><span data-stu-id="3810e-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="3810e-116">**GetInput**</span><span class="sxs-lookup"><span data-stu-id="3810e-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="3810e-117">Ottiene le variabili di input per un'attività.</span><span class="sxs-lookup"><span data-stu-id="3810e-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="3810e-118">**SetOutput**</span><span class="sxs-lookup"><span data-stu-id="3810e-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="3810e-119">Imposta le variabili di output per un'attività.</span><span class="sxs-lookup"><span data-stu-id="3810e-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="3810e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3810e-120">Requirements</span></span>



| <span data-ttu-id="3810e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3810e-121">Requirement</span></span> | <span data-ttu-id="3810e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3810e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3810e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3810e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3810e-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3810e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3810e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3810e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3810e-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3810e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3810e-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3810e-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="3810e-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3810e-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3810e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3810e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3810e-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3810e-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





