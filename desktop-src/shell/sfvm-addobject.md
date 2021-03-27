---
description: Aggiunge un oggetto alla visualizzazione Shell. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_ADDOBJECT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994888"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="ee743-104">\_Messaggio SFVM AddObject</span><span class="sxs-lookup"><span data-stu-id="ee743-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="ee743-105">Aggiunge un oggetto alla visualizzazione Shell.</span><span class="sxs-lookup"><span data-stu-id="ee743-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="ee743-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="ee743-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="ee743-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee743-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee743-108">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee743-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="ee743-109">Puntatore all'oggetto di interesse da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="ee743-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee743-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee743-110">Return value</span></span>

<span data-ttu-id="ee743-111">Restituisce il nuovo ID dell'elemento ListView dell'oggetto aggiunto se il processo ha avuto esito positivo; in caso contrario, restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="ee743-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee743-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee743-112">Requirements</span></span>



| <span data-ttu-id="ee743-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee743-113">Requirement</span></span> | <span data-ttu-id="ee743-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ee743-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee743-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee743-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee743-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee743-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ee743-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee743-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee743-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee743-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ee743-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee743-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee743-120"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee743-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




