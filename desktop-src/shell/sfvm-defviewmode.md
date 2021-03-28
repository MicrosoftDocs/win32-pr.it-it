---
description: "Consente all'oggetto callback di specificare la modalità di visualizzazione. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_DEFVIEWMODE (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995109"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="dd32c-104">\_Messaggio SFVM DEFVIEWMODE</span><span class="sxs-lookup"><span data-stu-id="dd32c-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="dd32c-105">Consente all'oggetto callback di specificare la modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dd32c-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="dd32c-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="dd32c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="dd32c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd32c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd32c-108">*pViewMode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd32c-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd32c-109">Uno dei valori del tipo enumerato [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .</span><span class="sxs-lookup"><span data-stu-id="dd32c-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd32c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd32c-110">Requirements</span></span>



| <span data-ttu-id="dd32c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd32c-111">Requirement</span></span> | <span data-ttu-id="dd32c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="dd32c-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dd32c-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd32c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dd32c-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd32c-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dd32c-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd32c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dd32c-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd32c-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dd32c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd32c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd32c-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd32c-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
