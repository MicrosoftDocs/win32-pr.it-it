---
title: TaskFolder.GetFolder - proprietà
description: Per lo scripting, ottiene una cartella che contiene le attività in un percorso specificato.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Proprietà GetFolder Utilità di pianificazione
- Proprietà GetFolder Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione proprietà , GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387030"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="221fd-106">TaskFolder.GetFolder - proprietà</span><span class="sxs-lookup"><span data-stu-id="221fd-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="221fd-107">Per lo scripting, ottiene una cartella che contiene le attività in un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="221fd-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="221fd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="221fd-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="221fd-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="221fd-109">Property value</span></span>

<span data-ttu-id="221fd-110">Percorso (percorso) della cartella.</span><span class="sxs-lookup"><span data-stu-id="221fd-110">The path (location) to the folder.</span></span> <span data-ttu-id="221fd-111">Non usare una barra rovesciata dopo l'ultimo nome di cartella nel percorso.</span><span class="sxs-lookup"><span data-stu-id="221fd-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="221fd-112">La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="221fd-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="221fd-113">Un esempio di percorso della cartella dell'attività, nella cartella dell'attività radice, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="221fd-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="221fd-114">Il carattere '.' non può essere usato per specificare la cartella attività corrente e '..'</span><span class="sxs-lookup"><span data-stu-id="221fd-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="221fd-115">Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="221fd-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="221fd-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="221fd-116">Error codes</span></span>

<span data-ttu-id="221fd-117">Cartella nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="221fd-117">The folder at the specified location.</span></span> <span data-ttu-id="221fd-118">La cartella è un [**oggetto TaskFolder.**](taskfolder.md)</span><span class="sxs-lookup"><span data-stu-id="221fd-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="221fd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="221fd-119">Requirements</span></span>



| <span data-ttu-id="221fd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="221fd-120">Requirement</span></span> | <span data-ttu-id="221fd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="221fd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="221fd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="221fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="221fd-123">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="221fd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="221fd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="221fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="221fd-125">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="221fd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="221fd-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="221fd-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="221fd-127"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="221fd-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="221fd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="221fd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="221fd-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="221fd-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





