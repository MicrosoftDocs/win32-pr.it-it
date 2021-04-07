---
title: Codice di notifica TBN_RESET (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti che l'utente ha reimpostato il contenuto della finestra di dialogo Personalizza barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- Controlli di Windows per il codice di notifica TBN_RESET
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048705"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="add51-105">\_Codice di notifica di reimpostazione TBN</span><span class="sxs-lookup"><span data-stu-id="add51-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="add51-106">Notifica alla finestra padre della barra degli strumenti che l'utente ha reimpostato il contenuto della finestra di dialogo Personalizza barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="add51-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="add51-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="add51-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="add51-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="add51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add51-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="add51-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="add51-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="add51-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add51-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="add51-111">Return value</span></span>

<span data-ttu-id="add51-112">Restituire TBNRF \_ ENDCUSTOMIZE per chiudere la finestra di dialogo Personalizza barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="add51-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="add51-113">Tutti gli altri valori restituiti vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="add51-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="add51-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="add51-114">Requirements</span></span>



| <span data-ttu-id="add51-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="add51-115">Requirement</span></span> | <span data-ttu-id="add51-116">Valore</span><span class="sxs-lookup"><span data-stu-id="add51-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="add51-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="add51-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="add51-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="add51-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="add51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="add51-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="add51-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="add51-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="add51-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="add51-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="add51-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





