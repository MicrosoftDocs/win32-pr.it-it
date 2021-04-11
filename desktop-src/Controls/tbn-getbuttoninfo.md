---
title: Codice di notifica TBN_GETBUTTONINFO (COMmctrl. h)
description: Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- Controlli di Windows per il codice di notifica TBN_GETBUTTONINFO
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964625"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="0735f-105">\_Codice di notifica GETBUTTONINFO di TBN</span><span class="sxs-lookup"><span data-stu-id="0735f-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="0735f-106">Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0735f-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="0735f-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0735f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0735f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0735f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0735f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0735f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0735f-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="0735f-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="0735f-111">Il membro **iItem** specifica un indice in base zero che fornisce un conteggio dei pulsanti nella finestra di dialogo Personalizza barra degli strumenti visualizzata come disponibile e presente sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0735f-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="0735f-112">Il membro **pszText** specifica l'indirizzo del testo del pulsante corrente e **cchText** ne specifica la lunghezza in caratteri.</span><span class="sxs-lookup"><span data-stu-id="0735f-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="0735f-113">L'applicazione deve riempire la struttura con informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="0735f-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0735f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0735f-114">Return value</span></span>

<span data-ttu-id="0735f-115">Restituisce **true** se le informazioni sul pulsante sono state copiate nella struttura specificata o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0735f-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0735f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0735f-116">Remarks</span></span>

<span data-ttu-id="0735f-117">Il controllo Toolbar alloca un buffer e il ricevitore (finestra padre) deve copiare il testo nel buffer.</span><span class="sxs-lookup"><span data-stu-id="0735f-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="0735f-118">Il membro **cchText** contiene la lunghezza del buffer allocato dalla barra degli strumenti quando TBN \_ GETBUTTONINFO viene inviato alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="0735f-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0735f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0735f-119">Requirements</span></span>



| <span data-ttu-id="0735f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0735f-120">Requirement</span></span> | <span data-ttu-id="0735f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0735f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0735f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0735f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0735f-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0735f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0735f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0735f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0735f-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0735f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0735f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0735f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0735f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0735f-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0735f-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0735f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0735f-129">**TBN \_ GETBUTTONINFOW** (Unicode) e **TBN \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0735f-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





