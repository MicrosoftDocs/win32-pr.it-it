---
description: "Consente all'oggetto callback di specificare che un'animazione deve essere visualizzata mentre gli elementi vengono enumerati in un thread in background. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Messaggio SFVM_GETANIMATION (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131950"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="d2d1a-104">\_Messaggio GETANIMATION SFVM</span><span class="sxs-lookup"><span data-stu-id="d2d1a-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="d2d1a-105">Consente all'oggetto callback di specificare che un'animazione deve essere visualizzata mentre gli elementi vengono enumerati in un thread in background.</span><span class="sxs-lookup"><span data-stu-id="d2d1a-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="d2d1a-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d2d1a-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="d2d1a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2d1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d1a-108">*phinst* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2d1a-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d1a-109">Handle dell'istanza del modulo da cui deve essere caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d2d1a-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="d2d1a-110">*pwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d2d1a-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d1a-111">Puntatore a una stringa Unicode con terminazione null che contiene il percorso del file AVI o il nome di una risorsa AVI.</span><span class="sxs-lookup"><span data-stu-id="d2d1a-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="d2d1a-112">In alternativa, questo parametro può essere costituito dall'identificatore di risorsa nella parola di basso livello e da 0 nella parola più significativa.</span><span class="sxs-lookup"><span data-stu-id="d2d1a-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="d2d1a-113">Per creare questo valore, usare la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="d2d1a-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="d2d1a-114">Il controllo carica la risorsa dal modulo specificato da hinst.</span><span class="sxs-lookup"><span data-stu-id="d2d1a-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="d2d1a-115">Una risorsa AVI deve avere il tipo "AVI".</span><span class="sxs-lookup"><span data-stu-id="d2d1a-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2d1a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2d1a-116">Remarks</span></span>

<span data-ttu-id="d2d1a-117">Per impostazione predefinita, l'oggetto visualizzazione cartella di sistema Visualizza l'animazione "torcia" durante un'enumerazione in background.</span><span class="sxs-lookup"><span data-stu-id="d2d1a-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="d2d1a-118">*phinst* e *pwszName* verranno passati al [controllo animazione](../controls/animation-control-overview.md) con un messaggio di [**\_ apertura ACM**](../controls/acm-open.md) .</span><span class="sxs-lookup"><span data-stu-id="d2d1a-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d1a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2d1a-119">Requirements</span></span>



| <span data-ttu-id="d2d1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d1a-120">Requirement</span></span> | <span data-ttu-id="d2d1a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d2d1a-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d1a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d1a-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2d1a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d2d1a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d1a-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2d1a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d2d1a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2d1a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2d1a-127"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d1a-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
