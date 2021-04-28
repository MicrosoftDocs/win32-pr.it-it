---
description: "DFM_WM_INITMENUPOPUP: inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu."
title: DFM_WM_INITMENUPOPUP messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096999"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="9bc0b-104">Messaggio \_ INITMENUPOPUP di DFM WM \_</span><span class="sxs-lookup"><span data-stu-id="9bc0b-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="9bc0b-105">Inviato quando un menu a discesa o un sottomenu sta per diventare attivo.</span><span class="sxs-lookup"><span data-stu-id="9bc0b-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="9bc0b-106">In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu.</span><span class="sxs-lookup"><span data-stu-id="9bc0b-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="9bc0b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bc0b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc0b-108">*wParam* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9bc0b-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc0b-109">Handle per il menu a discesa o il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="9bc0b-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="9bc0b-110">*lParam* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9bc0b-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc0b-111">La parola meno ordinata specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="9bc0b-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="9bc0b-112">La parola più importante indica se il menu a discesa è il menu della finestra.</span><span class="sxs-lookup"><span data-stu-id="9bc0b-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="9bc0b-113">Se il menu è il menu della finestra, questo parametro è **TRUE**; in caso contrario, è **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="9bc0b-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc0b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bc0b-114">Return value</span></span>

<span data-ttu-id="9bc0b-115">Se un'applicazione elabora questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="9bc0b-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc0b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc0b-116">Requirements</span></span>



| <span data-ttu-id="9bc0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc0b-117">Requirement</span></span> | <span data-ttu-id="9bc0b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc0b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc0b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc0b-120">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9bc0b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9bc0b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc0b-122">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9bc0b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9bc0b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bc0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bc0b-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc0b-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




