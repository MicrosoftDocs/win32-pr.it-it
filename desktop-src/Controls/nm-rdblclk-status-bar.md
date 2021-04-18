---
title: Codice di notifica di NM_RDBLCLK (barra di stato) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- Codice di notifica di NM_RDBLCLK (barra di stato) controlli Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18092b03a599c75a88deb56bb256d96728b96328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479420"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a><span data-ttu-id="0d873-105">\_Codice di notifica di RDBLCLK Nm (barra di stato)</span><span class="sxs-lookup"><span data-stu-id="0d873-105">NM\_RDBLCLK (status bar) notification code</span></span>

<span data-ttu-id="0d873-106">Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="0d873-106">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="0d873-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0d873-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0d873-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d873-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d873-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d873-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d873-110">Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="0d873-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="0d873-111">Il membro **dwItemSpec** contiene l'indice della sezione su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="0d873-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d873-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d873-112">Return value</span></span>

<span data-ttu-id="0d873-113">Restituisce **true** per indicare che il clic del mouse è stato gestito ed Elimina l'elaborazione predefinita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0d873-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="0d873-114">Restituisce **false** per consentire l'elaborazione predefinita del clic.</span><span class="sxs-lookup"><span data-stu-id="0d873-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d873-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d873-115">Requirements</span></span>



| <span data-ttu-id="0d873-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d873-116">Requirement</span></span> | <span data-ttu-id="0d873-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0d873-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d873-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d873-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d873-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d873-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d873-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d873-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d873-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d873-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d873-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d873-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d873-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d873-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





