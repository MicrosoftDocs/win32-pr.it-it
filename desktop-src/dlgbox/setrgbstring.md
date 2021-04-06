---
title: Messaggio SETRGBSTRING (COMMDLG. h)
description: La procedura di hook di una finestra di dialogo colore, CCHookProc, può inviare il messaggio registrato SETRGBSTRING alla finestra di dialogo per impostare la selezione del colore corrente.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Finestre di dialogo del messaggio SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742586"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="1ba35-104">Messaggio SETRGBSTRING</span><span class="sxs-lookup"><span data-stu-id="1ba35-104">SETRGBSTRING message</span></span>

<span data-ttu-id="1ba35-105">La procedura di hook di una finestra di dialogo **colore** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), può inviare il messaggio registrato **SETRGBSTRING** alla finestra di dialogo per impostare la selezione del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="1ba35-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="1ba35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ba35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ba35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ba35-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1ba35-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ba35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ba35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ba35-110">Valore RGB del colore da selezionare nella finestra di dialogo **colore** .</span><span class="sxs-lookup"><span data-stu-id="1ba35-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="1ba35-111">È possibile usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) per specificare le intensità rossa, verde e blu di un valore di colore RGB.</span><span class="sxs-lookup"><span data-stu-id="1ba35-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba35-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ba35-112">Return value</span></span>

<span data-ttu-id="1ba35-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="1ba35-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba35-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ba35-114">Remarks</span></span>

<span data-ttu-id="1ba35-115">Se *lParam* corrisponde a uno dei colori di base o a uno dei 16 colori personalizzati, la routine della finestra di dialogo Seleziona tale colore.</span><span class="sxs-lookup"><span data-stu-id="1ba35-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="1ba35-116">La routine della finestra di dialogo Aggiorna anche tutti i controlli nell'estensione di colore personalizzata della finestra di dialogo **colore** , se è aperta.</span><span class="sxs-lookup"><span data-stu-id="1ba35-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="1ba35-117">Se *lParam* non corrisponde a un colore di base o personalizzato, la procedura della finestra di dialogo non modifica la selezione di colore corrente, ma aggiorna i controlli colore personalizzati, se visibili.</span><span class="sxs-lookup"><span data-stu-id="1ba35-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="1ba35-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="1ba35-118">Examples</span></span>

<span data-ttu-id="1ba35-119">Il codice di esempio seguente ottiene l'identificatore del messaggio **SETRGBSTRING** , quindi imposta la selezione del colore su blu.</span><span class="sxs-lookup"><span data-stu-id="1ba35-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="1ba35-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ba35-120">Requirements</span></span>



| <span data-ttu-id="1ba35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba35-121">Requirement</span></span> | <span data-ttu-id="1ba35-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1ba35-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba35-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ba35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba35-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1ba35-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ba35-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ba35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba35-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1ba35-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ba35-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ba35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ba35-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ba35-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1ba35-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1ba35-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ba35-130">**SETRGBSTRINGW** (Unicode) e **SETRGBSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ba35-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="1ba35-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ba35-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ba35-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1ba35-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ba35-133">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="1ba35-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="1ba35-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="1ba35-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="1ba35-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="1ba35-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="1ba35-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1ba35-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ba35-137">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="1ba35-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

