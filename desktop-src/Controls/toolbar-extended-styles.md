---
title: Stili estesi barra degli strumenti (CommCtrl. h)
description: Questa sezione elenca gli stili estesi supportati dai controlli della barra degli strumenti.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326844"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="75a93-103">Stili estesi della barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="75a93-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="75a93-104">Questa sezione elenca gli stili estesi supportati dai controlli della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="75a93-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="75a93-105">Costante</span><span class="sxs-lookup"><span data-stu-id="75a93-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="75a93-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75a93-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="75a93-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="75a93-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="75a93-108"><a href="common-control-versions.md">Versione 4,71</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="75a93-109">Questo stile consente ai pulsanti di avere una freccia a discesa separata.</span><span class="sxs-lookup"><span data-stu-id="75a93-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="75a93-110">I pulsanti con lo stile <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> verranno disegnati con una freccia a discesa in una sezione separata, a destra del pulsante.</span><span class="sxs-lookup"><span data-stu-id="75a93-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="75a93-111">Se si fa clic sulla freccia, solo la parte freccia del pulsante verrà deselezionata e il controllo Toolbar invierà un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> codice di notifica per richiedere all'applicazione di visualizzare il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="75a93-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="75a93-112">Se si fa clic sulla parte principale del pulsante, il controllo Toolbar invia un messaggio di WM_COMMAND con l'ID del pulsante.</span><span class="sxs-lookup"><span data-stu-id="75a93-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="75a93-113">L'applicazione risponde normalmente avviando il primo comando nel menu.</span><span class="sxs-lookup"><span data-stu-id="75a93-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="75a93-114">In molti casi è possibile che si desideri disporre solo di alcuni pulsanti a discesa su una barra degli strumenti con frecce separate.</span><span class="sxs-lookup"><span data-stu-id="75a93-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="75a93-115">A tale scopo, impostare il TBSTYLE_EX_DRAWDDARROWS stile esteso.</span><span class="sxs-lookup"><span data-stu-id="75a93-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="75a93-116">Assegnare a questi pulsanti le frecce separate dallo stile <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75a93-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="75a93-117">Ai pulsanti con questo stile sarà visualizzata una freccia accanto all'immagine.</span><span class="sxs-lookup"><span data-stu-id="75a93-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="75a93-118">Tuttavia, la freccia non sarà separata e quando si fa clic su una parte del pulsante, il controllo Toolbar invierà un codice di notifica <a href="tbn-dropdown.md">TBN_DROPDOWN</a> .</span><span class="sxs-lookup"><span data-stu-id="75a93-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="75a93-119">Per evitare problemi di ridisegno, questo stile deve essere impostato prima che il controllo Toolbar diventi visibile.</span><span class="sxs-lookup"><span data-stu-id="75a93-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="75a93-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="75a93-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="75a93-121"><a href="common-control-versions.md">Versione 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="75a93-122">Questo stile nasconde i pulsanti parzialmente ritagliati.</span><span class="sxs-lookup"><span data-stu-id="75a93-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="75a93-123">L'uso più comune di questo stile è per le barre degli strumenti che fanno parte di un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="75a93-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="75a93-124">Se una banda adiacente copre parte di un pulsante, il pulsante non verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="75a93-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="75a93-125">Tuttavia, se la banda del controllo Rebar ha lo stile <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , il pulsante verrà visualizzato nel menu a discesa della freccia di espansione.</span><span class="sxs-lookup"><span data-stu-id="75a93-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="75a93-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="75a93-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="75a93-127"><a href="common-control-versions.md">Versione 6</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="75a93-128">Questo stile richiede il doppio buffer della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="75a93-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="75a93-129">Il doppio buffering è un meccanismo che rileva quando la barra degli strumenti è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="75a93-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75a93-130">Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="75a93-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="75a93-131">Per usare Comctl32.dll versione 6, specificarla in un manifesto.</span><span class="sxs-lookup"><span data-stu-id="75a93-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="75a93-132">Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="75a93-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="75a93-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="75a93-134"><a href="common-control-versions.md">Versione 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="75a93-135">Questo stile consente di impostare il testo per tutti i pulsanti, ma di visualizzarlo solo per i pulsanti con lo stile del pulsante <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75a93-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="75a93-136">È necessario impostare anche lo stile del <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75a93-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="75a93-137">In genere, quando un pulsante non Visualizza il testo, l'applicazione deve gestire <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> o <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> per visualizzare una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="75a93-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="75a93-138">Con il TBSTYLE_EX_MIXEDBUTTONS stile esteso, il testo impostato ma non visualizzato in un pulsante verrà usato automaticamente come testo della descrizione comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="75a93-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="75a93-139">L'applicazione deve gestire solo TBN_GETINFOTIP o o TTN_GETDISPINFO se è necessaria una maggiore flessibilità nella specifica del testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="75a93-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="75a93-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="75a93-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="75a93-141"><a href="common-control-versions.md">Versione 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="75a93-142"><strong>Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</strong></span><span class="sxs-lookup"><span data-stu-id="75a93-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="75a93-143">Questo stile assegna alla barra degli strumenti un orientamento verticale e organizza i pulsanti della barra degli strumenti in colonne.</span><span class="sxs-lookup"><span data-stu-id="75a93-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="75a93-144">I pulsanti scorrono verticalmente fino a quando un pulsante non ha superato l'altezza di delimitazione della barra degli strumenti (vedere <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) e quindi viene creata una nuova colonna.</span><span class="sxs-lookup"><span data-stu-id="75a93-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="75a93-145">La barra degli strumenti scorre i pulsanti in questo modo finché non vengono posizionati tutti i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="75a93-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="75a93-146">Per utilizzare questo stile, è necessario impostare anche lo stile del TBSTYLE_EX_VERTICAL.</span><span class="sxs-lookup"><span data-stu-id="75a93-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75a93-147">Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="75a93-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="75a93-148">Questo stile, inoltre, non è definito in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="75a93-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="75a93-149">Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="75a93-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="75a93-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="75a93-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="75a93-151"><a href="common-control-versions.md">Versione 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="75a93-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="75a93-152"><strong>Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</strong></span><span class="sxs-lookup"><span data-stu-id="75a93-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="75a93-153">Questo stile fornisce un orientamento verticale alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="75a93-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="75a93-154">I pulsanti della barra degli strumenti scorrono dall'alto verso il basso anziché orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="75a93-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75a93-155">Questo stile potrebbe non essere supportato nelle versioni future di Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="75a93-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="75a93-156">Questo stile, inoltre, non è definito in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="75a93-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="75a93-157">Aggiungere la definizione seguente ai file di origine dell'applicazione per usare questo stile: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="75a93-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="75a93-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="75a93-158">Remarks</span></span>

<span data-ttu-id="75a93-159">Per impostare uno stile esteso, inviare il controllo barra degli strumenti di un messaggio [**\_ SETEXTENDEDSTYLE TB**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="75a93-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="75a93-160">Per determinare gli stili estesi attualmente impostati, inviare un messaggio [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="75a93-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a93-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75a93-161">Requirements</span></span>



| <span data-ttu-id="75a93-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="75a93-162">Requirement</span></span> | <span data-ttu-id="75a93-163">Valore</span><span class="sxs-lookup"><span data-stu-id="75a93-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75a93-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75a93-164">Header</span></span><br/> | <dl> <span data-ttu-id="75a93-165"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75a93-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





