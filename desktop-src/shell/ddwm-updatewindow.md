---
description: Indica a una finestra rilascia immagine di eseguire l'aggiornamento usando le nuove informazioni DROPDESCRIPTION.
title: Messaggio DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977311"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="4c4cc-103">\_Messaggio DDWM UPDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="4c4cc-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="4c4cc-104">Indica a una finestra rilascia immagine di eseguire l'aggiornamento usando le nuove informazioni [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .</span><span class="sxs-lookup"><span data-stu-id="4c4cc-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c4cc-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c4cc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c4cc-106">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c4cc-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4cc-107">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4c4cc-108">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c4cc-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4cc-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c4cc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c4cc-110">Remarks</span></span>

<span data-ttu-id="4c4cc-111">DDWM \_ UPDATEWINDOW è definito come \_ utente WM + 3.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="4c4cc-112">Quando lo stato di un'operazione di eliminazione cambia, ad esempio in risposta a un tasto di modifica,[**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) restituisce un nuovo valore [**DropEffect**](../com/dropeffect-constants.md) (questo valore di **DropEffect** può essere ricevuto anche tramite [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span><span class="sxs-lookup"><span data-stu-id="4c4cc-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="4c4cc-113">In risposta, l'applicazione aggiorna la struttura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) della destinazione di rilascio con un nuovo valore [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) che indica la decorazione da applicare all'oggetto visivo della finestra di trascinamento. ad esempio, un'indicazione che indica che il file viene copiato anziché spostato o che l'oggetto non può essere eliminato in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="4c4cc-114">Tuttavia, gli oggetti visivi non vengono aggiornati finché l'oggetto riceve un messaggio **DDWM \_ UPDATEWINDOW** .</span><span class="sxs-lookup"><span data-stu-id="4c4cc-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="4c4cc-115">Il formato degli Appunti di [DragWindow](clipboard.md) fornisce l' **HWND** della finestra di trascinamento del destinatario al mittente del messaggio **\_ UPDATEWINDOW DDWM** .</span><span class="sxs-lookup"><span data-stu-id="4c4cc-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4cc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c4cc-116">Requirements</span></span>



| <span data-ttu-id="4c4cc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4cc-117">Requirement</span></span> | <span data-ttu-id="4c4cc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4c4cc-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c4cc-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c4cc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4cc-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c4cc-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c4cc-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c4cc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4cc-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c4cc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
