---
title: Struttura DLGITEMTEMPLATEEX
description: Blocco di testo utilizzato da un modello di finestra di dialogo esteso per descrivere la finestra di dialogo estesa. Per una descrizione del formato di un modello di finestra di dialogo esteso, vedere DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Finestre di dialogo struttura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400902"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="c7710-105">Struttura DLGITEMTEMPLATEEX</span><span class="sxs-lookup"><span data-stu-id="c7710-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="c7710-106">Blocco di testo utilizzato da un modello di finestra di dialogo esteso per descrivere la finestra di dialogo estesa.</span><span class="sxs-lookup"><span data-stu-id="c7710-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="c7710-107">Per una descrizione del formato di un modello di finestra di dialogo esteso, vedere [**DLGTEMPLATEEX**](dlgtemplateex.md).</span><span class="sxs-lookup"><span data-stu-id="c7710-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7710-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7710-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="c7710-109">Members</span><span class="sxs-lookup"><span data-stu-id="c7710-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7710-110">**helpID**</span><span class="sxs-lookup"><span data-stu-id="c7710-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7710-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-112">Identificatore del contesto della Guida per il controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-112">The help context identifier for the control.</span></span> <span data-ttu-id="c7710-113">Quando il sistema invia un messaggio della [**\_ Guida WM**](../shell/wm-help.md) , passa il valore **HelpID** nel membro **dwContextId** della struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="c7710-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-114">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="c7710-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7710-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-116">Stili estesi per una finestra.</span><span class="sxs-lookup"><span data-stu-id="c7710-116">The extended styles for a window.</span></span> <span data-ttu-id="c7710-117">Questo membro non viene utilizzato per creare controlli nelle finestre di dialogo, ma le applicazioni che utilizzano i modelli di finestra di dialogo possono utilizzarlo per creare altri tipi di finestre.</span><span class="sxs-lookup"><span data-stu-id="c7710-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="c7710-118">Per un elenco di valori, vedere [**stili finestra estesa**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="c7710-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="c7710-119">**style**</span><span class="sxs-lookup"><span data-stu-id="c7710-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-120">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7710-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-121">Stile del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-121">The style of the control.</span></span> <span data-ttu-id="c7710-122">Questo membro può essere una combinazione di [valori di stile della finestra](/windows/desktop/winmsg/window-styles) (ad esempio, il **\_ bordo WS**) e uno o più [valori dello stile del controllo](/windows/desktop/Controls/common-control-styles) , ad esempio il **\_ pulsante BS** e l' **es \_ Left**.</span><span class="sxs-lookup"><span data-stu-id="c7710-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="c7710-123">**x**</span><span class="sxs-lookup"><span data-stu-id="c7710-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-124">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="c7710-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-125">Coordinata x, in unità della finestra di dialogo, dell'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="c7710-126">Questa coordinata è sempre relativa all'angolo superiore sinistro dell'area client della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c7710-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-127">**y**</span><span class="sxs-lookup"><span data-stu-id="c7710-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-128">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="c7710-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-129">Coordinata y, in unità della finestra di dialogo, dell'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="c7710-130">Questa coordinata è sempre relativa all'angolo superiore sinistro dell'area client della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c7710-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-131">**CX**</span><span class="sxs-lookup"><span data-stu-id="c7710-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-132">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="c7710-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-133">Larghezza, in unità della finestra di dialogo, del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-134">**CY**</span><span class="sxs-lookup"><span data-stu-id="c7710-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-135">Tipo: **short**</span><span class="sxs-lookup"><span data-stu-id="c7710-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-136">Altezza, in unità della finestra di dialogo, del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-137">**id**</span><span class="sxs-lookup"><span data-stu-id="c7710-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-138">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7710-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-139">Identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-140">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="c7710-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-141">Tipo: **SZ \_ o \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="c7710-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-142">Matrice a lunghezza variabile di elementi a 16 bit che specifica la classe della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="c7710-143">Se il primo elemento di questa matrice è un valore diverso da 0xFFFF, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il nome di una classe di finestre registrate.</span><span class="sxs-lookup"><span data-stu-id="c7710-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="c7710-144">Se il primo elemento è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una classe di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="c7710-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="c7710-145">L'ordinale può essere uno dei valori Atom seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7710-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="c7710-146">Valore</span><span class="sxs-lookup"><span data-stu-id="c7710-146">Value</span></span>                                                                             | <span data-ttu-id="c7710-147">Significato</span><span class="sxs-lookup"><span data-stu-id="c7710-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="c7710-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="c7710-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="c7710-149">Pulsante</span><span class="sxs-lookup"><span data-stu-id="c7710-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="c7710-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="c7710-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="c7710-151">Modifica</span><span class="sxs-lookup"><span data-stu-id="c7710-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="c7710-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="c7710-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="c7710-153">Static</span><span class="sxs-lookup"><span data-stu-id="c7710-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="c7710-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="c7710-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="c7710-155">Casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="c7710-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="c7710-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="c7710-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="c7710-157">Barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="c7710-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="c7710-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="c7710-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="c7710-159">Casella combinata</span><span class="sxs-lookup"><span data-stu-id="c7710-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="c7710-160">**title**</span><span class="sxs-lookup"><span data-stu-id="c7710-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-161">Tipo: **SZ \_ o \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="c7710-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-162">Matrice a lunghezza variabile di elementi a 16 bit che contiene il testo iniziale o l'identificatore di risorsa del controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="c7710-163">Se il primo elemento di questa matrice è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una risorsa, ad esempio un'icona, in un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="c7710-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="c7710-164">È possibile usare un identificatore di risorsa per i controlli, ad esempio i controlli icona statici, che caricano e visualizzano un'icona o un'altra risorsa anziché il testo.</span><span class="sxs-lookup"><span data-stu-id="c7710-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="c7710-165">Se il primo elemento è un valore diverso da 0xFFFF, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il testo iniziale.</span><span class="sxs-lookup"><span data-stu-id="c7710-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="c7710-166">**Numero di ripetizioni**</span><span class="sxs-lookup"><span data-stu-id="c7710-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="c7710-167">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c7710-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c7710-168">Numero di byte di dati di creazione che seguono questo membro.</span><span class="sxs-lookup"><span data-stu-id="c7710-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="c7710-169">Se questo valore è maggiore di zero, i dati di creazione iniziano al confine di **parola** successivo.</span><span class="sxs-lookup"><span data-stu-id="c7710-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="c7710-170">I dati di creazione possono essere di qualsiasi dimensione e formato.</span><span class="sxs-lookup"><span data-stu-id="c7710-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="c7710-171">La routine della finestra del controllo deve essere in grado di interpretare i dati.</span><span class="sxs-lookup"><span data-stu-id="c7710-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="c7710-172">Quando il sistema crea il controllo, passa un puntatore a questi dati nel parametro *lParam* del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) inviato al controllo.</span><span class="sxs-lookup"><span data-stu-id="c7710-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7710-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7710-173">Remarks</span></span>

<span data-ttu-id="c7710-174">Un modello esteso per una finestra di dialogo è costituito da un'intestazione [**DLGTEMPLATEEX**](dlgtemplateex.md) seguita da una struttura **DLGITEMTEMPLATEEX** per ogni controllo nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c7710-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="c7710-175">Ogni struttura **DLGITEMTEMPLATEEX** deve essere allineata su un limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c7710-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="c7710-176">Le matrici **WindowClass** e **title** a lunghezza variabile devono essere allineate sui limiti di **parola** .</span><span class="sxs-lookup"><span data-stu-id="c7710-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="c7710-177">La matrice di dati di creazione, se presente, deve essere allineata su un confine di **parola** .</span><span class="sxs-lookup"><span data-stu-id="c7710-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="c7710-178">Se si specificano stringhe di caratteri nelle matrici **WindowClass** e **title** , è necessario utilizzare stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7710-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="c7710-179">Utilizzare la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare stringhe Unicode da stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="c7710-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="c7710-180">I membri **x**, **y**, **CX** e **CY** specificano i valori nelle unità della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c7710-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="c7710-181">È possibile convertire questi valori in unità schermo (pixel) utilizzando la funzione [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="c7710-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7710-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7710-182">Requirements</span></span>



| <span data-ttu-id="c7710-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7710-183">Requirement</span></span> | <span data-ttu-id="c7710-184">Valore</span><span class="sxs-lookup"><span data-stu-id="c7710-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c7710-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7710-185">Minimum supported client</span></span><br/> | <span data-ttu-id="c7710-186">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c7710-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c7710-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7710-187">Minimum supported server</span></span><br/> | <span data-ttu-id="c7710-188">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c7710-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c7710-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7710-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7710-190">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c7710-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7710-191">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="c7710-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="c7710-192">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="c7710-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="c7710-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="c7710-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="c7710-194">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="c7710-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="c7710-195">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="c7710-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="c7710-196">**DLGTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="c7710-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="c7710-197">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="c7710-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="c7710-198">**creazione di WM \_**</span><span class="sxs-lookup"><span data-stu-id="c7710-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="c7710-199">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c7710-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7710-200">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="c7710-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="c7710-201">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="c7710-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c7710-202">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="c7710-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="c7710-203">**Guida di WM \_**</span><span class="sxs-lookup"><span data-stu-id="c7710-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

