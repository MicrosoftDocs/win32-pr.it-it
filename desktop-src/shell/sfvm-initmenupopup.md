---
description: "Consente all'oggetto callback di modificare un menu a comparsa di Esplora risorse prima che venga visualizzato. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_INITMENUPOPUP (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980834"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="2dff5-104">\_Messaggio SFVM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="2dff5-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="2dff5-105">Consente all'oggetto callback di modificare un menu a comparsa di Esplora risorse prima che venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2dff5-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="2dff5-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="2dff5-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="2dff5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dff5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dff5-108">*idCmd \_ nIndex* \[\]</span><span class="sxs-lookup"><span data-stu-id="2dff5-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dff5-109">La parola più bassa di questo parametro include il valore del primo ID comando riservato per i comandi client.</span><span class="sxs-lookup"><span data-stu-id="2dff5-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="2dff5-110">La parola più ordinata include l'indice del menu.</span><span class="sxs-lookup"><span data-stu-id="2dff5-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="2dff5-111">*HMENU* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2dff5-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dff5-112">Handle del menu.</span><span class="sxs-lookup"><span data-stu-id="2dff5-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dff5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dff5-113">Remarks</span></span>

<span data-ttu-id="2dff5-114">L'oggetto visualizzazione cartella di sistema invia questo messaggio quando viene selezionato un menu, ma prima che venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2dff5-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="2dff5-115">Elaborare questo messaggio se, ad esempio, è necessario abilitare o disabilitare i comandi di menu.</span><span class="sxs-lookup"><span data-stu-id="2dff5-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="2dff5-116">Il menu popup può essere:</span><span class="sxs-lookup"><span data-stu-id="2dff5-116">The popup menu can be:</span></span>

-   <span data-ttu-id="2dff5-117">Menu file, modifica o Visualizza.</span><span class="sxs-lookup"><span data-stu-id="2dff5-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="2dff5-118">Menu di primo livello definito dal client.</span><span class="sxs-lookup"><span data-stu-id="2dff5-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="2dff5-119">Sottomenu definito dal client.</span><span class="sxs-lookup"><span data-stu-id="2dff5-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dff5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dff5-120">Requirements</span></span>



| <span data-ttu-id="2dff5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dff5-121">Requirement</span></span> | <span data-ttu-id="2dff5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2dff5-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2dff5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dff5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2dff5-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2dff5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2dff5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dff5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2dff5-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2dff5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2dff5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2dff5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dff5-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dff5-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dff5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dff5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dff5-130">**\_MERGEMENU SFVM**</span><span class="sxs-lookup"><span data-stu-id="2dff5-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
