---
title: Messaggio WM_SYSCOMMAND (winuser. h)
description: Una finestra riceve questo messaggio quando l'utente sceglie un comando dal menu finestra (noto in precedenza come menu di sistema o di controllo) o quando l'utente sceglie il pulsante Ingrandisci, Riduci a icona, pulsante Ripristina o Chiudi.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- Menu del messaggio WM_SYSCOMMAND e altre risorse
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330437"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="7074a-104">\_Messaggio SYSCOMMAND WM</span><span class="sxs-lookup"><span data-stu-id="7074a-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="7074a-105">Una finestra riceve questo messaggio quando l'utente sceglie un comando dal menu **finestra** (noto in precedenza come menu di sistema o di controllo) o quando l'utente sceglie il pulsante Ingrandisci, Riduci a icona, pulsante Ripristina o Chiudi.</span><span class="sxs-lookup"><span data-stu-id="7074a-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="7074a-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="7074a-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="7074a-107">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="7074a-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="7074a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7074a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7074a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7074a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7074a-110">Tipo di comando di sistema richiesto.</span><span class="sxs-lookup"><span data-stu-id="7074a-110">The type of system command requested.</span></span> <span data-ttu-id="7074a-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7074a-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7074a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7074a-112">Value</span></span></th>
<th><span data-ttu-id="7074a-113">Significato</span><span class="sxs-lookup"><span data-stu-id="7074a-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="7074a-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-115">Chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="7074a-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-117">Imposta il cursore su un punto interrogativo con un puntatore.</span><span class="sxs-lookup"><span data-stu-id="7074a-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="7074a-118">Se l'utente fa clic su un controllo nella finestra di dialogo, il controllo riceve un messaggio di <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7074a-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="7074a-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-120">Seleziona l'elemento predefinito. l'utente ha fatto doppio clic sul menu finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="7074a-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-122">Attiva la finestra associata al tasto di scelta rapida specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7074a-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="7074a-123">Il parametro <em>lParam</em> identifica la finestra da attivare.</span><span class="sxs-lookup"><span data-stu-id="7074a-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="7074a-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-125">Scorre orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="7074a-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="7074a-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-127">Indica se la screen saver è protetta.</span><span class="sxs-lookup"><span data-stu-id="7074a-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="7074a-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-129">Recupera il menu finestra come risultato di una sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="7074a-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="7074a-130">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7074a-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="7074a-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-132">Ingrandisce la finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="7074a-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-134">Riduce a icona la finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="7074a-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-136">Imposta lo stato della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7074a-136">Sets the state of the display.</span></span> <span data-ttu-id="7074a-137">Questo comando supporta i dispositivi che dispongono di funzionalità di risparmio energia, ad esempio un personal computer alimentato da batteria.</span><span class="sxs-lookup"><span data-stu-id="7074a-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="7074a-138">Il parametro <em>lParam</em> può includere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7074a-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="7074a-139">-1 (lo schermo è acceso)</span><span class="sxs-lookup"><span data-stu-id="7074a-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="7074a-140">1 (lo schermo sarà a basso consumo)</span><span class="sxs-lookup"><span data-stu-id="7074a-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="7074a-141">2 (lo schermo sta per essere spento)</span><span class="sxs-lookup"><span data-stu-id="7074a-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="7074a-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-143">Recupera il menu finestra a seguito di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="7074a-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="7074a-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-145">Sposta la finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="7074a-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-147">Passa alla finestra successiva.</span><span class="sxs-lookup"><span data-stu-id="7074a-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="7074a-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-149">Passa alla finestra precedente.</span><span class="sxs-lookup"><span data-stu-id="7074a-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="7074a-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-151">Ripristina la posizione e le dimensioni normali della finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="7074a-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-153">Esegue l'applicazione screen saver specificata nella sezione [boot] del file di System.ini.</span><span class="sxs-lookup"><span data-stu-id="7074a-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="7074a-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-155">Ridimensiona la finestra.</span><span class="sxs-lookup"><span data-stu-id="7074a-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="7074a-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-157">Attiva il menu <strong>Start</strong> .</span><span class="sxs-lookup"><span data-stu-id="7074a-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="7074a-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span><span class="sxs-lookup"><span data-stu-id="7074a-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="7074a-159">Scorre verticalmente.</span><span class="sxs-lookup"><span data-stu-id="7074a-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="7074a-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7074a-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7074a-161">La parola di ordine inferiore specifica la posizione orizzontale del cursore, in coordinate dello schermo, se si sceglie un comando di menu finestra con il mouse.</span><span class="sxs-lookup"><span data-stu-id="7074a-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="7074a-162">In caso contrario, questo parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7074a-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="7074a-163">La parola più ordinata specifica la posizione verticale del cursore, in coordinate dello schermo, se si sceglie un comando di menu finestra con il mouse.</span><span class="sxs-lookup"><span data-stu-id="7074a-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="7074a-164">Questo parametro è 1 se il comando viene scelto utilizzando un acceleratore di sistema oppure zero se si utilizza un tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="7074a-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7074a-165">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7074a-165">Return value</span></span>

<span data-ttu-id="7074a-166">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="7074a-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7074a-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="7074a-167">Remarks</span></span>

<span data-ttu-id="7074a-168">Per ottenere le coordinate di posizione nelle coordinate dello schermo, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="7074a-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="7074a-169">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esegue la richiesta del menu finestra per le azioni predefinite specificate nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="7074a-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="7074a-170">Nei messaggi **WM \_ SYSCOMMAND** , i quattro bit di ordine inferiore del parametro *wParam* vengono usati internamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="7074a-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="7074a-171">Per ottenere il risultato corretto durante il test del valore di *wParam*, un'applicazione deve combinare il valore 0xFFF0 con il valore *wParam* usando l'operatore and bit per bit.</span><span class="sxs-lookup"><span data-stu-id="7074a-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="7074a-172">È possibile modificare le voci di menu in un menu finestra usando le funzioni [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="7074a-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="7074a-173">Le applicazioni che modificano il menu finestra devono elaborare i messaggi **WM \_ SYSCOMMAND** .</span><span class="sxs-lookup"><span data-stu-id="7074a-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="7074a-174">Un'applicazione può eseguire qualsiasi comando di sistema in qualsiasi momento passando un messaggio **WM \_ SYSCOMMAND** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="7074a-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="7074a-175">Tutti i messaggi **WM \_ SYSCOMMAND** non gestiti dall'applicazione devono essere passati a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="7074a-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="7074a-176">Qualsiasi valore di comando aggiunto da un'applicazione deve essere elaborato dall'applicazione e non può essere passato a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="7074a-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="7074a-177">Se la protezione con password è abilitata dal criterio, l'screen saver viene avviata indipendentemente dalle operazioni svolte da un'applicazione con la notifica **SC \_ SCREENSAVE** , anche se non riesce a passarla a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="7074a-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="7074a-178">I tasti di scelta rapida definiti per scegliere gli elementi dal menu finestra vengono convertiti in messaggi **WM \_ SYSCOMMAND** . tutte le altre sequenze di tasti di scelta rapida vengono convertite in messaggi di [**\_ comando WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="7074a-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="7074a-179">Se il *wParam* è **il \_ menu chiavi SC**, *lParam* contiene il codice carattere della chiave utilizzata con il tasto ALT per visualizzare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="7074a-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="7074a-180">Ad esempio, se si preme ALT + F per visualizzare il popup del file, un **WM \_ SYSCOMMAND** con *wParam* uguale a **SC \_** e *lParam* è uguale a' F '.</span><span class="sxs-lookup"><span data-stu-id="7074a-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="7074a-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7074a-181">Requirements</span></span>



| <span data-ttu-id="7074a-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="7074a-182">Requirement</span></span> | <span data-ttu-id="7074a-183">Valore</span><span class="sxs-lookup"><span data-stu-id="7074a-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7074a-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7074a-184">Minimum supported client</span></span><br/> | <span data-ttu-id="7074a-185">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7074a-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7074a-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7074a-186">Minimum supported server</span></span><br/> | <span data-ttu-id="7074a-187">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7074a-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7074a-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7074a-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="7074a-189"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7074a-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7074a-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7074a-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="7074a-191">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7074a-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7074a-192">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="7074a-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="7074a-193">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7074a-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7074a-194">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="7074a-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="7074a-195">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="7074a-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="7074a-196">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="7074a-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="7074a-197">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="7074a-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="7074a-198">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="7074a-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="7074a-199">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="7074a-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="7074a-200">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7074a-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7074a-201">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="7074a-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

