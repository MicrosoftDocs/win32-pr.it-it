---
description: Inviato alla finestra padre di un controllo o di un menu creato dal proprietario quando un aspetto visivo del controllo o del menu è stato modificato.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Messaggio DFM_WM_DRAWITEM (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977266"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="8039b-103">\_Messaggio DFM WM \_ DrawItem</span><span class="sxs-lookup"><span data-stu-id="8039b-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="8039b-104">Inviato alla finestra padre di un controllo o di un menu creato dal proprietario quando un aspetto visivo del controllo o del menu è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8039b-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="8039b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8039b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8039b-106">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8039b-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8039b-107">Identificatore del controllo che ha inviato il messaggio **DFM \_ WM \_ DrawItem** .</span><span class="sxs-lookup"><span data-stu-id="8039b-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="8039b-108">Se il messaggio è stato inviato da un menu, questo parametro è zero.</span><span class="sxs-lookup"><span data-stu-id="8039b-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="8039b-109">*lpDrawItem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8039b-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8039b-110">Puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenente le informazioni sull'elemento da disegnare e il tipo di disegno necessario.</span><span class="sxs-lookup"><span data-stu-id="8039b-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8039b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8039b-111">Return value</span></span>

<span data-ttu-id="8039b-112">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="8039b-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8039b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8039b-113">Remarks</span></span>

<span data-ttu-id="8039b-114">Il membro **itemAction** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) specifica l'operazione di disegno che deve essere eseguita da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8039b-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="8039b-115">Prima di restituire l'elaborazione di questo messaggio, un'applicazione deve garantire che il contesto di dispositivo identificato dal membro **HDC** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sia nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="8039b-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="8039b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8039b-116">Requirements</span></span>



| <span data-ttu-id="8039b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8039b-117">Requirement</span></span> | <span data-ttu-id="8039b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8039b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8039b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8039b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8039b-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8039b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8039b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8039b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8039b-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8039b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8039b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8039b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8039b-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8039b-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
