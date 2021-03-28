---
description: Notifica a IShellView di ridisporre gli elementi. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_REARRANGE (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058288"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="dff1a-104">SFVM \_ ridisposizione messaggio</span><span class="sxs-lookup"><span data-stu-id="dff1a-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="dff1a-105">Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) di ridisporre gli elementi.</span><span class="sxs-lookup"><span data-stu-id="dff1a-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="dff1a-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="dff1a-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="dff1a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dff1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff1a-108">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dff1a-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff1a-109">Passata a [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span><span class="sxs-lookup"><span data-stu-id="dff1a-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="dff1a-110">Per ulteriori informazioni su questo parametro, vedere [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) .</span><span class="sxs-lookup"><span data-stu-id="dff1a-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff1a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dff1a-111">Return value</span></span>

<span data-ttu-id="dff1a-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="dff1a-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dff1a-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dff1a-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dff1a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dff1a-114">Requirements</span></span>



| <span data-ttu-id="dff1a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dff1a-115">Requirement</span></span> | <span data-ttu-id="dff1a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dff1a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dff1a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dff1a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dff1a-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dff1a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dff1a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dff1a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dff1a-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dff1a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dff1a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dff1a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff1a-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff1a-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




