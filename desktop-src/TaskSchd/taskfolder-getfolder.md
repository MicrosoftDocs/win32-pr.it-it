---
title: Proprietà TaskFolder. GetFolder
description: Per gli script, ottiene una cartella che contiene le attività in una posizione specificata.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Utilità di pianificazione proprietà GetFolder
- Utilità di pianificazione proprietà GetFolder, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà GetFolder
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
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119291"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="f9dca-106">Proprietà TaskFolder. GetFolder</span><span class="sxs-lookup"><span data-stu-id="f9dca-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="f9dca-107">Per gli script, ottiene una cartella che contiene le attività in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f9dca-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9dca-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="f9dca-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f9dca-109">Property value</span></span>

<span data-ttu-id="f9dca-110">Percorso (percorso) della cartella.</span><span class="sxs-lookup"><span data-stu-id="f9dca-110">The path (location) to the folder.</span></span> <span data-ttu-id="f9dca-111">Non usare una barra rovesciata che segue il nome dell'ultima cartella nel percorso.</span><span class="sxs-lookup"><span data-stu-id="f9dca-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="f9dca-112">La cartella radice dell'attività è specificata con una barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="f9dca-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="f9dca-113">Un esempio di percorso di una cartella attività, nella cartella radice dell'attività, è \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="f9dca-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="f9dca-114">Non è possibile usare il carattere ' .' per specificare la cartella attività corrente è. .'</span><span class="sxs-lookup"><span data-stu-id="f9dca-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="f9dca-115">non è possibile utilizzare i caratteri per specificare la cartella attività padre nel percorso.</span><span class="sxs-lookup"><span data-stu-id="f9dca-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9dca-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f9dca-116">Error codes</span></span>

<span data-ttu-id="f9dca-117">Cartella nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="f9dca-117">The folder at the specified location.</span></span> <span data-ttu-id="f9dca-118">La cartella è un oggetto [**TaskFolder**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="f9dca-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dca-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9dca-119">Requirements</span></span>



| <span data-ttu-id="f9dca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9dca-120">Requirement</span></span> | <span data-ttu-id="f9dca-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f9dca-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dca-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9dca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dca-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9dca-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f9dca-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9dca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dca-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9dca-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9dca-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f9dca-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9dca-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9dca-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9dca-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f9dca-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9dca-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9dca-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





