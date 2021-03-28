---
description: "Notifica all'oggetto callback del sito contenitore. Viene usato solo quando IObjectWithSite:: SESITE non è supportato e viene usato SHCreateShellFolderViewEx. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Messaggio SFVM_SETISFV (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980879"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="9d238-105">\_Messaggio SFVM SETISFV</span><span class="sxs-lookup"><span data-stu-id="9d238-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="9d238-106">\[Questa notifica è supportata tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d238-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="9d238-107">Potrebbe non essere supportata nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9d238-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9d238-108">Notifica all'oggetto callback del sito contenitore.</span><span class="sxs-lookup"><span data-stu-id="9d238-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="9d238-109">Viene usato solo quando [**IObjectWithSite:: SESITE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) non è supportato e viene usato [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) .</span><span class="sxs-lookup"><span data-stu-id="9d238-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="9d238-110">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="9d238-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="9d238-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d238-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d238-112">*sito* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9d238-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d238-113">Puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sito contenitore.</span><span class="sxs-lookup"><span data-stu-id="9d238-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d238-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d238-114">Requirements</span></span>



| <span data-ttu-id="9d238-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d238-115">Requirement</span></span> | <span data-ttu-id="9d238-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9d238-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d238-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d238-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d238-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9d238-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9d238-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d238-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d238-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9d238-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d238-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d238-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d238-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d238-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
