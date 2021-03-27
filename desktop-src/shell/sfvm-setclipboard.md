---
description: Notifica a IShellView quando uno dei relativi oggetti viene inserito negli Appunti come risultato di un comando di menu. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_SETCLIPBOARD (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995157"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="74789-104">SFVM \_ messaggi degli Appunti</span><span class="sxs-lookup"><span data-stu-id="74789-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="74789-105">Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quando uno dei relativi oggetti viene inserito negli Appunti come risultato di un comando di menu.</span><span class="sxs-lookup"><span data-stu-id="74789-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="74789-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="74789-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="74789-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="74789-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74789-108">*dwEffect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74789-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74789-109">Use (WPARAM)-2 se l'elemento viene tagliato negli Appunti o (WPARAM)-3 Se l'elemento viene copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="74789-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74789-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74789-110">Return value</span></span>

<span data-ttu-id="74789-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="74789-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74789-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="74789-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="74789-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74789-113">Requirements</span></span>



| <span data-ttu-id="74789-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="74789-114">Requirement</span></span> | <span data-ttu-id="74789-115">Valore</span><span class="sxs-lookup"><span data-stu-id="74789-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74789-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74789-116">Minimum supported client</span></span><br/> | <span data-ttu-id="74789-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74789-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74789-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74789-118">Minimum supported server</span></span><br/> | <span data-ttu-id="74789-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74789-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74789-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74789-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="74789-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="74789-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




