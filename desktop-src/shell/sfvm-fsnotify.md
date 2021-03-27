---
description: "Notifica all'oggetto callback che si è verificato un evento che interessa uno dei relativi elementi. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_FSNOTIFY (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "104995221"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="fe57c-104">\_Messaggio SFVM FSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="fe57c-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="fe57c-105">Notifica all'oggetto callback che si è verificato un evento che interessa uno dei relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="fe57c-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="fe57c-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="fe57c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="fe57c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe57c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe57c-108">*ppidl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe57c-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57c-109">Puntatore di PIDL dell'elemento interessato.</span><span class="sxs-lookup"><span data-stu-id="fe57c-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="fe57c-110">*Levent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe57c-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe57c-111">Valore SHCNE che indica l'evento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="fe57c-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="fe57c-112">Per un elenco di valori possibili, vedere [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span><span class="sxs-lookup"><span data-stu-id="fe57c-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe57c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe57c-113">Requirements</span></span>



| <span data-ttu-id="fe57c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe57c-114">Requirement</span></span> | <span data-ttu-id="fe57c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fe57c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe57c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe57c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe57c-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe57c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe57c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe57c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe57c-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe57c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe57c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe57c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe57c-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe57c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
