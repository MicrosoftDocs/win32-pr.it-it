---
description: "Notifica all'oggetto callback che è in corso la creazione della finestra di visualizzazione cartelle. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_WINDOWCREATED (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980866"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="39588-104">\_Messaggio SFVM WINDOWCREATED</span><span class="sxs-lookup"><span data-stu-id="39588-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="39588-105">Notifica all'oggetto callback che è in corso la creazione della finestra di visualizzazione cartelle.</span><span class="sxs-lookup"><span data-stu-id="39588-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="39588-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="39588-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="39588-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="39588-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39588-108">*hwndView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39588-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39588-109">Handle della finestra della visualizzazione cartelle.</span><span class="sxs-lookup"><span data-stu-id="39588-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39588-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39588-110">Requirements</span></span>



| <span data-ttu-id="39588-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="39588-111">Requirement</span></span> | <span data-ttu-id="39588-112">Valore</span><span class="sxs-lookup"><span data-stu-id="39588-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39588-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39588-113">Minimum supported client</span></span><br/> | <span data-ttu-id="39588-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39588-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="39588-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39588-115">Minimum supported server</span></span><br/> | <span data-ttu-id="39588-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39588-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39588-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39588-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="39588-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="39588-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
