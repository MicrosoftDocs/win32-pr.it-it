---
title: Messaggio TB_ADDBUTTONS (COMmctrl. h)
description: Aggiunge uno o più pulsanti a una barra degli strumenti.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Controlli di Windows Message TB_ADDBUTTONS
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965006"
---
# <a name="tb_addbuttons-message"></a><span data-ttu-id="f7700-104">TB \_ ADDBUTTONS messaggio</span><span class="sxs-lookup"><span data-stu-id="f7700-104">TB\_ADDBUTTONS message</span></span>

<span data-ttu-id="f7700-105">Aggiunge uno o più pulsanti a una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f7700-105">Adds one or more buttons to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7700-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7700-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7700-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7700-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7700-108">Numero di pulsanti da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f7700-108">Number of buttons to add.</span></span>

</dd> <dt>

<span data-ttu-id="f7700-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7700-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7700-110">Puntatore a una matrice di strutture [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che contengono informazioni sui pulsanti da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f7700-110">Pointer to an array of [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures that contain information about the buttons to add.</span></span> <span data-ttu-id="f7700-111">Il numero di elementi nella matrice deve essere uguale a quello dei pulsanti specificati da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f7700-111">There must be the same number of elements in the array as buttons specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7700-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7700-112">Return value</span></span>

<span data-ttu-id="f7700-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f7700-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7700-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7700-114">Remarks</span></span>

<span data-ttu-id="f7700-115">Se la barra degli strumenti è stata creata utilizzando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , è necessario inviare il messaggio [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) alla barra degli strumenti prima di inviare **TB \_ ADDBUTTONS**.</span><span class="sxs-lookup"><span data-stu-id="f7700-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBUTTONS**.</span></span>

<span data-ttu-id="f7700-116">Per una discussione su come assegnare bitmap ai pulsanti della barra degli strumenti da uno o più elenchi di immagini, vedere [**TB \_ seimagine**](tb-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="f7700-116">See [**TB\_SETIMAGELIST**](tb-setimagelist.md) for a discussion of how to assign bitmaps to toolbar buttons from one or more image lists.</span></span>

## <a name="examples"></a><span data-ttu-id="f7700-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="f7700-117">Examples</span></span>

<span data-ttu-id="f7700-118">Il codice di esempio seguente aggiunge tre pulsanti a una barra degli strumenti, usando la bitmap di sistema standard per i pulsanti di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f7700-118">The following example code adds three buttons to a toolbar, using the standard system bitmap for view buttons.</span></span> <span data-ttu-id="f7700-119">Il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) restituisce l'indice della prima immagine del pulsante all'interno dell'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="f7700-119">The [**TB\_ADDBITMAP**](tb-addbitmap.md) message returns the index of the first button image within the image list.</span></span> <span data-ttu-id="f7700-120">Le singole immagini vengono identificate in base ai relativi offset da tale valore.</span><span class="sxs-lookup"><span data-stu-id="f7700-120">Individual images are identified by their offsets from that value.</span></span>


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a><span data-ttu-id="f7700-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7700-121">Requirements</span></span>



| <span data-ttu-id="f7700-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7700-122">Requirement</span></span> | <span data-ttu-id="f7700-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f7700-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7700-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7700-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7700-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7700-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7700-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7700-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7700-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7700-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7700-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7700-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7700-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7700-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f7700-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f7700-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f7700-131">**TB \_ ADDBUTTONSW** (Unicode) e **TB \_ ADDBUTTONSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f7700-131">**TB\_ADDBUTTONSW** (Unicode) and **TB\_ADDBUTTONSA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f7700-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7700-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7700-133">**Valori di indice dell'immagine del pulsante standard della barra degli strumenti**</span><span class="sxs-lookup"><span data-stu-id="f7700-133">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

