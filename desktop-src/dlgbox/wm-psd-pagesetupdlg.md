---
title: Messaggio WM_PSD_PAGESETUPDLG (COMMDLG. h)
description: Notifica a una procedura PagePaintHook hook che la finestra di dialogo Imposta pagina sta per creare il contenuto della pagina di esempio. La procedura hook può utilizzare questo messaggio per eseguire attività di inizializzazione correlate alla creazione del contenuto della pagina di esempio.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- Finestre di dialogo WM_PSD_PAGESETUPDLG messaggio
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400900"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="39b52-105">\_ \_ Messaggio PAGESETUPDLG di WM PSD</span><span class="sxs-lookup"><span data-stu-id="39b52-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="39b52-106">Notifica a una procedura [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook che la finestra di dialogo **Imposta pagina** sta per creare il contenuto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="39b52-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="39b52-107">La procedura hook può utilizzare questo messaggio per eseguire attività di inizializzazione correlate alla creazione del contenuto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="39b52-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="39b52-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39b52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b52-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39b52-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39b52-110">La parola di ordine inferiore specifica un valore che indica il formato della carta.</span><span class="sxs-lookup"><span data-stu-id="39b52-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="39b52-111">Questo valore può essere uno dei valori **DMPAPER \_** elencati nella descrizione della struttura.</span><span class="sxs-lookup"><span data-stu-id="39b52-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="39b52-112">La parola più significativa specifica l'orientamento della carta o della busta e indica se la stampante è una matrice di punti o un dispositivo HPPCL (Hewlett Packard Printer Control Language).</span><span class="sxs-lookup"><span data-stu-id="39b52-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="39b52-113">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="39b52-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="39b52-114">Valore</span><span class="sxs-lookup"><span data-stu-id="39b52-114">Value</span></span>                                                                             | <span data-ttu-id="39b52-115">Significato</span><span class="sxs-lookup"><span data-stu-id="39b52-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="39b52-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="39b52-117">Carta in modalità orizzontale (matrice di punti)</span><span class="sxs-lookup"><span data-stu-id="39b52-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="39b52-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="39b52-119">Carta in modalità orizzontale (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="39b52-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="39b52-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="39b52-121">Carta in modalità verticale (matrice a punti)</span><span class="sxs-lookup"><span data-stu-id="39b52-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="39b52-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="39b52-123">Carta in modalità verticale (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="39b52-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="39b52-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="39b52-125">Busta in modalità orizzontale (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="39b52-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="39b52-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="39b52-127">Busta in modalità verticale (matrice di punti)</span><span class="sxs-lookup"><span data-stu-id="39b52-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="39b52-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="39b52-129">Busta in modalità orizzontale (matrice di punti)</span><span class="sxs-lookup"><span data-stu-id="39b52-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="39b52-130"><dt>0x001F</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="39b52-131">Busta in modalità verticale (HPPCL)</span><span class="sxs-lookup"><span data-stu-id="39b52-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="39b52-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39b52-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39b52-133">Puntatore a una struttura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) contenente le informazioni utilizzate per inizializzare la finestra di dialogo **Imposta pagina** .</span><span class="sxs-lookup"><span data-stu-id="39b52-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b52-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39b52-134">Return value</span></span>

<span data-ttu-id="39b52-135">Se la procedura di hook restituisce **true**, la finestra di dialogo non invia più messaggi e non viene disegnato nella pagina di esempio fino alla successiva necessità di ricreare la pagina di esempio dal sistema.</span><span class="sxs-lookup"><span data-stu-id="39b52-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="39b52-136">Se la routine hook restituisce **false**, la finestra di dialogo Invia i messaggi rimanenti della sequenza di disegno.</span><span class="sxs-lookup"><span data-stu-id="39b52-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b52-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="39b52-137">Remarks</span></span>

<span data-ttu-id="39b52-138">Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="39b52-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="39b52-139">Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="39b52-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="39b52-140">Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="39b52-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="39b52-141">I primi tre messaggi di una sequenza di disegno (**WM \_ PSD \_ PAGESETUPDLG**, [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)o [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)) forniscono informazioni che la procedura hook può utilizzare per disegnare il contenuto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="39b52-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="39b52-142">I messaggi rimanenti [**(WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md), [**WM \_ PSD \_ GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM \_ PSD \_ ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM \_ PSD \_ YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notificano alla procedura hook che la finestra di dialogo sta per creare una parte specifica della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="39b52-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="39b52-143">Questo consente alla routine hook di creare selettivamente parti della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="39b52-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b52-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39b52-144">Requirements</span></span>



| <span data-ttu-id="39b52-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="39b52-145">Requirement</span></span> | <span data-ttu-id="39b52-146">Valore</span><span class="sxs-lookup"><span data-stu-id="39b52-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b52-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39b52-147">Minimum supported client</span></span><br/> | <span data-ttu-id="39b52-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39b52-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39b52-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39b52-149">Minimum supported server</span></span><br/> | <span data-ttu-id="39b52-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="39b52-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39b52-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39b52-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b52-152"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39b52-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b52-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39b52-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="39b52-154">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="39b52-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39b52-155">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="39b52-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="39b52-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39b52-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="39b52-157">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="39b52-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="39b52-158">**\_ENVSTAMPRECT PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="39b52-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="39b52-159">**\_FULLPAGERECT PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="39b52-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="39b52-160">**\_GREEKTEXTRECT PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="39b52-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="39b52-161">**\_MARGINRECT PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="39b52-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="39b52-162">**\_MINMARGINRECT PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="39b52-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="39b52-163">**\_YAFULLPAGERECT PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="39b52-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="39b52-164">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="39b52-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="39b52-165">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="39b52-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

