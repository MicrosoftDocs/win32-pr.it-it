---
description: Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu.
title: Messaggio DFM_WM_INITMENUPOPUP (Shlobj. h)
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
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128451"
---
# <a name="dfm_wm_initmenupopup-message"></a><span data-ttu-id="d2df0-104">DFM \_ WM \_ INITMENUPOPUP messaggio</span><span class="sxs-lookup"><span data-stu-id="d2df0-104">DFM\_WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="d2df0-105">Inviato quando un menu a discesa o un sottomenu sta per diventare attivo.</span><span class="sxs-lookup"><span data-stu-id="d2df0-105">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="d2df0-106">Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu.</span><span class="sxs-lookup"><span data-stu-id="d2df0-106">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a><span data-ttu-id="d2df0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2df0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2df0-108">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2df0-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2df0-109">Handle per il menu a discesa o il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="d2df0-109">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="d2df0-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2df0-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2df0-111">La parola di ordine inferiore specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.</span><span class="sxs-lookup"><span data-stu-id="d2df0-111">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="d2df0-112">La parola più ordinata indica se il menu a discesa è il menu finestra.</span><span class="sxs-lookup"><span data-stu-id="d2df0-112">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="d2df0-113">Se il menu è il menu finestra, questo parametro è **true**; in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2df0-113">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2df0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2df0-114">Return value</span></span>

<span data-ttu-id="d2df0-115">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="d2df0-115">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2df0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2df0-116">Requirements</span></span>



| <span data-ttu-id="d2df0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2df0-117">Requirement</span></span> | <span data-ttu-id="d2df0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d2df0-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d2df0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2df0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2df0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2df0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d2df0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2df0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2df0-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2df0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d2df0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2df0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2df0-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2df0-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




