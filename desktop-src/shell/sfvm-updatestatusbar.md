---
description: "Notifica all'oggetto di callback che la barra di stato è in fase di aggiornamento. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_UPDATESTATUSBAR (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994813"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="28ad9-104">\_Messaggio SFVM UPDATESTATUSBAR</span><span class="sxs-lookup"><span data-stu-id="28ad9-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="28ad9-105">Notifica all'oggetto di callback che la barra di stato è in fase di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28ad9-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="28ad9-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="28ad9-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="28ad9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="28ad9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ad9-108">*fInitialize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28ad9-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ad9-109">Valore **bool** che è impostato su **true** se la barra di stato è in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="28ad9-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28ad9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="28ad9-110">Remarks</span></span>

<span data-ttu-id="28ad9-111">Quando si riceve la notifica:</span><span class="sxs-lookup"><span data-stu-id="28ad9-111">When you receive this notification:</span></span>

-   <span data-ttu-id="28ad9-112">Restituisce \_ OK se si gestirà l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28ad9-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="28ad9-113">Return MAKE \_ HRESULT (SEverity \_ Success, 0, 1) per fare in modo che l'oggetto visualizzazione cartella di sistema imposti il testo della barra di stato.</span><span class="sxs-lookup"><span data-stu-id="28ad9-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="28ad9-114">Return E \_ non consentono all'oggetto visualizzazione cartella di sistema di gestire la barra di stato.</span><span class="sxs-lookup"><span data-stu-id="28ad9-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="28ad9-115">Il testo della barra di stato predefinito è il seguente.</span><span class="sxs-lookup"><span data-stu-id="28ad9-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="28ad9-116">Stato</span><span class="sxs-lookup"><span data-stu-id="28ad9-116">Status</span></span>                      | <span data-ttu-id="28ad9-117">Testo barra di stato</span><span class="sxs-lookup"><span data-stu-id="28ad9-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="28ad9-118">Nessun elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="28ad9-118">No items selected</span></span>           | <span data-ttu-id="28ad9-119">" \# \# oggetti" (nella cartella)</span><span class="sxs-lookup"><span data-stu-id="28ad9-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="28ad9-120">Un elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="28ad9-120">One item selected</span></span>           | <span data-ttu-id="28ad9-121">Infotip per l'elemento, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="28ad9-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="28ad9-122">Più di un elemento selezionato</span><span class="sxs-lookup"><span data-stu-id="28ad9-122">More than one item selected</span></span> | <span data-ttu-id="28ad9-123">" \# \# oggetti selezionati"</span><span class="sxs-lookup"><span data-stu-id="28ad9-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="28ad9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28ad9-124">Requirements</span></span>



| <span data-ttu-id="28ad9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ad9-125">Requirement</span></span> | <span data-ttu-id="28ad9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="28ad9-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28ad9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28ad9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="28ad9-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28ad9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28ad9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28ad9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="28ad9-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28ad9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="28ad9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28ad9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="28ad9-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ad9-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
