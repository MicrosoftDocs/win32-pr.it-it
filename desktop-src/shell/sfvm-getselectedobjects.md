---
description: Recupera una matrice di puntatori a elenchi di identificatori di elemento (PIDL) per tutti gli oggetti selezionati. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_GETSELECTEDOBJECTS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885341"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="cd7c9-104">\_Messaggio SFVM GETSELECTEDOBJECTS</span><span class="sxs-lookup"><span data-stu-id="cd7c9-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="cd7c9-105">Recupera una matrice di puntatori a elenchi di identificatori di elemento (PIDL) per tutti gli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="cd7c9-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="cd7c9-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="cd7c9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd7c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7c9-108">*ppidl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd7c9-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="cd7c9-109">Indirizzo di una matrice di PIDL di oggetti attualmente selezionati.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7c9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd7c9-110">Return value</span></span>

<span data-ttu-id="cd7c9-111">Restituisce il numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7c9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd7c9-112">Remarks</span></span>

<span data-ttu-id="cd7c9-113">Al termine, è necessario chiamare [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) su ogni membro della matrice per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7c9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd7c9-114">Requirements</span></span>



| <span data-ttu-id="cd7c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7c9-115">Requirement</span></span> | <span data-ttu-id="cd7c9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cd7c9-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7c9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd7c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7c9-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd7c9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cd7c9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd7c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7c9-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd7c9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cd7c9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd7c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd7c9-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd7c9-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




