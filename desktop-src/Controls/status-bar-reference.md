---
title: Barra di stato
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli barra di stato.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731490"
---
# <a name="status-bar"></a><span data-ttu-id="282f8-103">Barra di stato</span><span class="sxs-lookup"><span data-stu-id="282f8-103">Status Bar</span></span>

<span data-ttu-id="282f8-104">Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli barra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="282f8-105">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="282f8-105">Overviews</span></span>



| <span data-ttu-id="282f8-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="282f8-106">Topic</span></span>                          | <span data-ttu-id="282f8-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="282f8-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="282f8-108">Barre di stato</span><span class="sxs-lookup"><span data-stu-id="282f8-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="282f8-109">Una *barra di stato* è una finestra orizzontale nella parte inferiore di una finestra padre in cui un'applicazione può visualizzare vari tipi di informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="282f8-110">Funzioni</span><span class="sxs-lookup"><span data-stu-id="282f8-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="282f8-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="282f8-111">Topic</span></span></th>
<th><span data-ttu-id="282f8-112">Contenuto</span><span class="sxs-lookup"><span data-stu-id="282f8-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="282f8-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="282f8-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="282f8-114">Crea una finestra di stato, che in genere viene utilizzata per visualizzare lo stato di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="282f8-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="282f8-115">La finestra viene in genere visualizzata nella parte inferiore della finestra padre e contiene il testo specificato.</span><span class="sxs-lookup"><span data-stu-id="282f8-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="282f8-116">questa funzione è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="282f8-116">This function is obsolete.</span></span> <span data-ttu-id="282f8-117">In alternativa, usare <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="282f8-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="282f8-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span><span class="sxs-lookup"><span data-stu-id="282f8-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="282f8-119">La funzione <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> disegna il testo specificato nello stile di una finestra di stato con bordi.</span><span class="sxs-lookup"><span data-stu-id="282f8-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="282f8-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="282f8-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="282f8-121">Elabora <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> e <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> i messaggi e visualizza il testo della guida sul menu corrente nella finestra di stato specificata.</span><span class="sxs-lookup"><span data-stu-id="282f8-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="282f8-122">Messaggi</span><span class="sxs-lookup"><span data-stu-id="282f8-122">Messages</span></span>



| <span data-ttu-id="282f8-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="282f8-123">Topic</span></span>                                               | <span data-ttu-id="282f8-124">Contenuto</span><span class="sxs-lookup"><span data-stu-id="282f8-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="282f8-125">**SB \_ GETborders**</span><span class="sxs-lookup"><span data-stu-id="282f8-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="282f8-126">Recupera le larghezze correnti dei bordi orizzontali e verticali di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="282f8-127">**SB \_ GETicon**</span><span class="sxs-lookup"><span data-stu-id="282f8-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="282f8-128">Recupera l'icona per una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="282f8-129">**SB \_ GETparts**</span><span class="sxs-lookup"><span data-stu-id="282f8-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="282f8-130">Recupera un conteggio delle parti in una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="282f8-131">Il messaggio recupera inoltre la coordinata del bordo destro del numero di parti specificato.</span><span class="sxs-lookup"><span data-stu-id="282f8-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="282f8-132">**SB \_ GETrect**</span><span class="sxs-lookup"><span data-stu-id="282f8-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="282f8-133">Recupera il rettangolo di delimitazione di una parte in una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="282f8-134">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="282f8-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="282f8-135">Il messaggio [**SB \_ gettext**](sb-gettext.md) Recupera il testo dalla parte specificata di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="282f8-136">**\_GETTEXTLENGTH SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="282f8-137">Il messaggio [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="282f8-138">**\_GETTIPTEXT SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="282f8-139">Recupera il testo della descrizione comando per una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="282f8-140">La barra di stato deve essere creata con lo stile della [**\_ Descrizione comando SBT**](status-bar-styles.md) per abilitare le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="282f8-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="282f8-141">**\_GETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="282f8-142">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="282f8-143">**\_semplice SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="282f8-144">Controlla un controllo barra di stato per determinare se è in modalità semplice.</span><span class="sxs-lookup"><span data-stu-id="282f8-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="282f8-145">**\_SETBKCOLOR SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="282f8-146">Imposta il colore di sfondo di una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="282f8-147">**\_icona SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="282f8-148">Imposta l'icona di una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="282f8-149">**\_SETMINHEIGHT SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="282f8-150">Imposta l'altezza minima dell'area di disegno di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="282f8-151">**sottoparti SB \_**</span><span class="sxs-lookup"><span data-stu-id="282f8-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="282f8-152">Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.</span><span class="sxs-lookup"><span data-stu-id="282f8-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="282f8-153">**\_testo SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="282f8-154">Il messaggio SB SetText \_ imposta il testo nella parte specificata di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="282f8-155">**\_SETTIPTEXT SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="282f8-156">Imposta il testo della descrizione comando per una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="282f8-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="282f8-157">La barra di stato deve essere stata creata con lo stile [**SBT \_ Tooltips**](status-bar-styles.md) per abilitare le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="282f8-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="282f8-158">**\_SETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="282f8-159">Imposta il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="282f8-160">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="282f8-161">**\_semplice SB**</span><span class="sxs-lookup"><span data-stu-id="282f8-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="282f8-162">Specifica se una finestra di stato Visualizza testo semplice o Visualizza tutte le parti della finestra impostate da un messaggio precedente della [**\_ parte SB**](sb-setparts.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="282f8-163">Notifiche</span><span class="sxs-lookup"><span data-stu-id="282f8-163">Notifications</span></span>



| <span data-ttu-id="282f8-164">Argomento</span><span class="sxs-lookup"><span data-stu-id="282f8-164">Topic</span></span>                                                 | <span data-ttu-id="282f8-165">Contenuto</span><span class="sxs-lookup"><span data-stu-id="282f8-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="282f8-166">\_Clic su Nm (barra di stato)</span><span class="sxs-lookup"><span data-stu-id="282f8-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="282f8-167">Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="282f8-168">[Nm \_ FARE clic su (barra di stato)](nm-click-status-bar.md) viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="282f8-169">NM \_ DBLCLK (barra di stato)</span><span class="sxs-lookup"><span data-stu-id="282f8-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="282f8-170">Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="282f8-171">Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="282f8-172">NM \_ RCLICK (barra di stato)</span><span class="sxs-lookup"><span data-stu-id="282f8-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="282f8-173">Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="282f8-174">Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="282f8-175">NM \_ RDBLCLK (barra di stato)</span><span class="sxs-lookup"><span data-stu-id="282f8-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="282f8-176">Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="282f8-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="282f8-177">[Nm \_ RDBLCLK (barra di stato)](nm-rdblclk-status-bar.md) viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="282f8-178">\_SIMPLEMODECHANGE SBN</span><span class="sxs-lookup"><span data-stu-id="282f8-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="282f8-179">Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un messaggio [**\_ semplice SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="282f8-180">Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="282f8-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="282f8-181">Costanti</span><span class="sxs-lookup"><span data-stu-id="282f8-181">Constants</span></span>



| <span data-ttu-id="282f8-182">Argomento</span><span class="sxs-lookup"><span data-stu-id="282f8-182">Topic</span></span>                                      | <span data-ttu-id="282f8-183">Contenuto</span><span class="sxs-lookup"><span data-stu-id="282f8-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="282f8-184">Stili della barra di stato</span><span class="sxs-lookup"><span data-stu-id="282f8-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="282f8-185">Questa sezione elenca gli stili, oltre agli stili standard della finestra, supportati dai controlli *barra di stato* .</span><span class="sxs-lookup"><span data-stu-id="282f8-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

