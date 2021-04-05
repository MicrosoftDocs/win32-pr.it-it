---
title: Messaggio HDM_LAYOUT (COMmctrl. h)
description: Recupera le informazioni utilizzate per impostare le dimensioni e la posizione del controllo intestazione all'interno del rettangolo di destinazione della finestra padre. È possibile inviare questo messaggio in modo esplicito o usare la macro del layout dell'intestazione \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Controlli di Windows Message HDM_LAYOUT
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048394"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="f5004-105">\_Messaggio layout HDM</span><span class="sxs-lookup"><span data-stu-id="f5004-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="f5004-106">Recupera le informazioni utilizzate per impostare le dimensioni e la posizione del controllo intestazione all'interno del rettangolo di destinazione della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="f5004-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="f5004-107">È possibile inviare questo messaggio in modo esplicito o usare la macro del [**\_ layout dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .</span><span class="sxs-lookup"><span data-stu-id="f5004-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5004-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5004-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5004-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5004-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f5004-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f5004-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f5004-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5004-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5004-112">Puntatore a una struttura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) .</span><span class="sxs-lookup"><span data-stu-id="f5004-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="f5004-113">Il membro **PRC** specifica le coordinate di un rettangolo e il membro **pwpos** riceve le dimensioni e la posizione del controllo intestazione all'interno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="f5004-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5004-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5004-114">Return value</span></span>

<span data-ttu-id="f5004-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f5004-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5004-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5004-116">Remarks</span></span>

<span data-ttu-id="f5004-117">Il membro **pwpos** della struttura *lParam* riceve i valori di dimensioni e posizioni appropriati per posizionare il controllo lungo la parte superiore del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="f5004-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="f5004-118">Il valore altezza è la somma delle altezze dei bordi orizzontali del controllo e l'altezza media dei caratteri nel tipo di carattere attualmente selezionato nel contesto di dispositivo del controllo.</span><span class="sxs-lookup"><span data-stu-id="f5004-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="f5004-119">Per usare **il \_ layout HDM** per impostare le dimensioni iniziali e la posizione di un controllo intestazione, impostare lo stato di visibilità iniziale del controllo in modo che sia nascosto.</span><span class="sxs-lookup"><span data-stu-id="f5004-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="f5004-120">Dopo aver inviato il **\_ layout HDM** per recuperare i valori di dimensioni e posizione, usare la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) per impostare la nuova dimensione, la posizione e lo stato di visibilità.</span><span class="sxs-lookup"><span data-stu-id="f5004-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5004-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5004-121">Requirements</span></span>



| <span data-ttu-id="f5004-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5004-122">Requirement</span></span> | <span data-ttu-id="f5004-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f5004-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5004-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5004-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f5004-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5004-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5004-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5004-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f5004-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5004-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5004-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5004-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5004-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5004-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

