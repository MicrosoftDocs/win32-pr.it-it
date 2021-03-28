---
description: 'Consente al callback di modificare i \_ valori cfm xxx passati a IContextMenu:: QueryContextMenu.'
title: Messaggio DFM_MODIFYQCMFLAGS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878766"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="3506a-103">\_Messaggio DFM MODIFYQCMFLAGS</span><span class="sxs-lookup"><span data-stu-id="3506a-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="3506a-104">Consente al callback di modificare i \_ valori cfm xxx passati a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3506a-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="3506a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3506a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3506a-106">*puNewFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3506a-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3506a-107">Puntatore ai nuovi valori del flag.</span><span class="sxs-lookup"><span data-stu-id="3506a-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="3506a-108">*uFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3506a-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3506a-109">Flag che specificano il modo in cui il menu di scelta rapida può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="3506a-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="3506a-110">Questo parametro usa i \_ valori di CMF xxx descritti in [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3506a-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3506a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3506a-111">Requirements</span></span>



| <span data-ttu-id="3506a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3506a-112">Requirement</span></span> | <span data-ttu-id="3506a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3506a-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3506a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3506a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3506a-115">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3506a-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3506a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3506a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3506a-117">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3506a-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3506a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3506a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3506a-119"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3506a-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




