---
description: SFVM \_ THISIDLIST può essere modificato o non disponibile.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Messaggio SFVM_THISIDLIST (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760196"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="6c793-103">\_Messaggio SFVM THISIDLIST</span><span class="sxs-lookup"><span data-stu-id="6c793-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="6c793-104">\[**SFVM \_ THISIDLIST** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6c793-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c793-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="6c793-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6c793-106">Consente all'oggetto callback di specificare il puntatore della visualizzazione a un elenco di identificatori di elemento (PIDL).</span><span class="sxs-lookup"><span data-stu-id="6c793-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="6c793-107">Viene usato solo quando [**IPersistIDList:: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) e [**IPersistFolder2:: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) hanno avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6c793-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="6c793-108">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6c793-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="6c793-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c793-110">*PIDL* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c793-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c793-111">Indirizzo della PIDL della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c793-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c793-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c793-112">Requirements</span></span>



| <span data-ttu-id="6c793-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c793-113">Requirement</span></span> | <span data-ttu-id="6c793-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6c793-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c793-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c793-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c793-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6c793-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c793-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c793-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c793-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c793-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c793-119">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6c793-119">End of client support</span></span><br/>    | <span data-ttu-id="6c793-120">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="6c793-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="6c793-121">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6c793-121">End of server support</span></span><br/>    | <span data-ttu-id="6c793-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c793-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="6c793-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c793-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c793-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c793-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
