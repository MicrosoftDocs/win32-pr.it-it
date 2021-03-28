---
description: Aggiorna un oggetto passando un puntatore a una matrice di due puntatori a elenchi di identificatori di elemento (PIDL). Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_UPDATEOBJECT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234085"
---
# <a name="sfvm_updateobject-message"></a><span data-ttu-id="1452c-104">\_Messaggio SFVM UPDATEOBJECT</span><span class="sxs-lookup"><span data-stu-id="1452c-104">SFVM\_UPDATEOBJECT message</span></span>

<span data-ttu-id="1452c-105">Aggiorna un oggetto passando un puntatore a una matrice di due puntatori a elenchi di identificatori di elemento (PIDL).</span><span class="sxs-lookup"><span data-stu-id="1452c-105">Updates an object by passing a pointer to an array of two pointers to item identifier lists (PIDLs).</span></span> <span data-ttu-id="1452c-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="1452c-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="1452c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1452c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1452c-108">*ppidl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1452c-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1452c-109">Indirizzo di una matrice di due PIDL.</span><span class="sxs-lookup"><span data-stu-id="1452c-109">The address of an array of two PIDLs.</span></span> <span data-ttu-id="1452c-110">Il primo PIDL è il PIDL precedente.</span><span class="sxs-lookup"><span data-stu-id="1452c-110">The first PIDL is the old PIDL.</span></span> <span data-ttu-id="1452c-111">Il secondo è una copia del vecchio PIDL con le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="1452c-111">The second one is a copy of the old PIDL with updated information.</span></span> <span data-ttu-id="1452c-112">Il controllo della durata della copia appartiene alla visualizzazione dopo il completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="1452c-112">Control over the copy's lifetime belongs to the view after successful completion of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1452c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1452c-113">Return value</span></span>

<span data-ttu-id="1452c-114">Restituisce l'ID ListView dell'oggetto aggiornato se l'aggiornamento è stato eseguito correttamente. in caso contrario, restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="1452c-114">Returns the listview ID of the updated object if the update was successful; otherwise, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1452c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1452c-115">Remarks</span></span>

<span data-ttu-id="1452c-116">Se l'aggiornamento non è riuscito, il chiamante deve liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="1452c-116">If the update was unsuccessful, the caller must free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="1452c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1452c-117">Requirements</span></span>



| <span data-ttu-id="1452c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1452c-118">Requirement</span></span> | <span data-ttu-id="1452c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1452c-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1452c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1452c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1452c-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1452c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1452c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1452c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1452c-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1452c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1452c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1452c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1452c-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1452c-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




