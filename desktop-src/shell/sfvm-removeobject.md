---
description: Rimuove un oggetto dalla visualizzazione Shell. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_REMOVEOBJECT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980887"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="3a5ce-104">\_Messaggio SFVM RemoveObject</span><span class="sxs-lookup"><span data-stu-id="3a5ce-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="3a5ce-105">Rimuove un oggetto dalla visualizzazione Shell.</span><span class="sxs-lookup"><span data-stu-id="3a5ce-105">Removes an object from the shell view.</span></span> <span data-ttu-id="3a5ce-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="3a5ce-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="3a5ce-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a5ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5ce-108">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5ce-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="3a5ce-109">PIDL dell'oggetto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3a5ce-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5ce-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a5ce-110">Return value</span></span>

<span data-ttu-id="3a5ce-111">Restituisce l'indice dell'elemento che è stato rimosso se è stato trovato un elemento corrispondente all'oggetto PIDL specificato. in caso contrario, restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="3a5ce-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5ce-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3a5ce-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5ce-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a5ce-113">Requirements</span></span>



| <span data-ttu-id="3a5ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a5ce-114">Requirement</span></span> | <span data-ttu-id="3a5ce-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3a5ce-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5ce-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5ce-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a5ce-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3a5ce-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5ce-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a5ce-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3a5ce-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a5ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5ce-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5ce-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




