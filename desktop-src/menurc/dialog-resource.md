---
title: Risorsa finestra di dialogo
description: Definisce una finestra di dialogo. | Risorsa finestra di dialogo
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- Menu delle risorse della finestra di dialogo e altre risorse
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321318"
---
# <a name="dialog-resource"></a><span data-ttu-id="ad5e5-105">Risorsa finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="ad5e5-105">DIALOG resource</span></span>

<span data-ttu-id="ad5e5-106">Definisce una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-106">Defines a dialog box.</span></span> <span data-ttu-id="ad5e5-107">L'istruzione definisce la posizione e le dimensioni della finestra di dialogo sullo schermo nonché lo stile della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="ad5e5-108">La **finestra di dialogo** è un ID di risorsa obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="ad5e5-109">Le nuove applicazioni devono usare [**DIALOGEX**](dialogex-resource.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="ad5e5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad5e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad5e5-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="ad5e5-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="ad5e5-112">Nome univoco o valore di Unsigned Integer a 16 bit univoco che identifica la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="ad5e5-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*</span><span class="sxs-lookup"><span data-stu-id="ad5e5-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="ad5e5-114">Opzioni per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-114">Options for the dialog box.</span></span> <span data-ttu-id="ad5e5-115">Questa operazione può essere costituita da zero o più delle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="ad5e5-116">Istruzione</span><span class="sxs-lookup"><span data-stu-id="ad5e5-116">Statement</span></span>                                                        | <span data-ttu-id="ad5e5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad5e5-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5e5-118">[**Didascalia**](caption-statement.md) "*testo*"</span><span class="sxs-lookup"><span data-stu-id="ad5e5-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="ad5e5-119">Didascalia della finestra di dialogo se dispone di una barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="ad5e5-120">Per ulteriori informazioni, vedere la [**didascalia**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="ad5e5-121">[**Caratteristiche**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="ad5e5-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="ad5e5-122">Valore **DWORD** definito dall'utente per l'utilizzo da strumenti di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="ad5e5-123">Questo valore non viene utilizzato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-123">This value is not used by the system.</span></span> <span data-ttu-id="ad5e5-124">Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="ad5e5-125">[](class-statement.md) *Classe* Class</span><span class="sxs-lookup"><span data-stu-id="ad5e5-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="ad5e5-126">Unsigned Integer a 16 bit o una stringa racchiusa tra virgolette doppie ("), che identifica la classe della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="ad5e5-127">Per ulteriori informazioni, vedere la [**classe**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="ad5e5-128">**ExStyle =** *stili estesi*</span><span class="sxs-lookup"><span data-stu-id="ad5e5-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="ad5e5-129">Stile finestra esteso della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="ad5e5-130">Per ulteriori informazioni, vedere [**ExStyle**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="ad5e5-131">**Carattere** *pointsize*, carattere *tipografico*</span><span class="sxs-lookup"><span data-stu-id="ad5e5-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="ad5e5-132">Dimensioni del punto e carattere tipografico per il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-132">Point size and typeface for the font.</span></span> <span data-ttu-id="ad5e5-133">Per ulteriori informazioni, vedere [**carattere**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="ad5e5-134">[](language-statement.md) *Lingua* lingua, *lingua*</span><span class="sxs-lookup"><span data-stu-id="ad5e5-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="ad5e5-135">Lingua della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-135">Language of the dialog box.</span></span> <span data-ttu-id="ad5e5-136">Per ulteriori informazioni, vedere [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="ad5e5-137"> *Menu* menu</span><span class="sxs-lookup"><span data-stu-id="ad5e5-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="ad5e5-138">Menu da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-138">Menu to be used.</span></span> <span data-ttu-id="ad5e5-139">Questo valore è il nome del menu o il relativo identificatore di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="ad5e5-140">[](style-statement.md) *Stili* di stile</span><span class="sxs-lookup"><span data-stu-id="ad5e5-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="ad5e5-141">Stili della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-141">Styles of the dialog box.</span></span> <span data-ttu-id="ad5e5-142">Per ulteriori informazioni, vedere [**stile**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="ad5e5-143">[](version-statement.md) *DWORD* versione</span><span class="sxs-lookup"><span data-stu-id="ad5e5-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="ad5e5-144">Valore **DWORD** definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="ad5e5-145">Questa istruzione è destinata all'utilizzo da parte di altri strumenti di risorse e non viene utilizzata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="ad5e5-146">Per ulteriori informazioni, vedere [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="ad5e5-147">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="ad5e5-148">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e5-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5e5-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad5e5-149">Remarks</span></span>

<span data-ttu-id="ad5e5-150">La funzione [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) restituisce le unità di base della finestra di dialogo in pixel.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="ad5e5-151">Il significato esatto delle coordinate dipende dallo stile definito dall'istruzione di opzione [**Style**](style-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5e5-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="ad5e5-152">Per le finestre di dialogo di tipo figlio, le coordinate sono relative all'origine della finestra padre, a meno che la finestra di dialogo non disponga dello stile **DS \_ ABSALIGN**; in tal caso, le coordinate sono relative all'origine della schermata di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="ad5e5-153">Non usare lo stile **WS \_ figlio** con una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="ad5e5-154">La funzione [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) Disabilita sempre il padre/proprietario della finestra di dialogo appena creata.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="ad5e5-155">Quando una finestra padre è disabilitata, le finestre figlio vengono disabilitate in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="ad5e5-156">Poiché la finestra padre della finestra di dialogo di tipo figlio è disabilitata, la finestra di dialogo di tipo figlio è anch ' essa.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="ad5e5-157">Se una finestra di dialogo ha lo stile **DS \_ ABSALIGN** , le coordinate della finestra di dialogo per l'angolo superiore sinistro sono relative all'origine dello schermo anziché all'angolo superiore sinistro della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="ad5e5-158">Questo stile viene in genere utilizzato quando si desidera che la finestra di dialogo venga avviata in una parte specifica della visualizzazione, indipendentemente dalla posizione in cui è possibile che la finestra padre si trovi sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="ad5e5-159">La finestra di **dialogo** nome può essere usata anche come parametro Class-Name per la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per creare una finestra con gli attributi della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="ad5e5-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="ad5e5-160">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad5e5-160">Examples</span></span>

<span data-ttu-id="ad5e5-161">Di seguito viene illustrato l'utilizzo dell'istruzione della **finestra di dialogo** :</span><span class="sxs-lookup"><span data-stu-id="ad5e5-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="ad5e5-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad5e5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5e5-163">Utilizzo delle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="ad5e5-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-164">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-165">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-166">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-167">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="ad5e5-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="ad5e5-169">**DialogBox**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="ad5e5-170">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="ad5e5-171">**LINGUAGGIO**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-172">**MENU**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-174">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="ad5e5-175">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ad5e5-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
