---
title: Stili del controllo intestazione (CommCtrl. h)
description: I controlli Header hanno diversi stili, descritti in questa sezione, che determinano l'aspetto e il comportamento del controllo. È possibile impostare gli stili iniziali durante la creazione del controllo intestazione.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327241"
---
# <a name="header-control-styles"></a><span data-ttu-id="60ab1-104">Stili del controllo intestazione</span><span class="sxs-lookup"><span data-stu-id="60ab1-104">Header Control Styles</span></span>

<span data-ttu-id="60ab1-105">I controlli Header hanno diversi stili, descritti in questa sezione, che determinano l'aspetto e il comportamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="60ab1-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="60ab1-106">È possibile impostare gli stili iniziali durante la creazione del controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="60ab1-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="60ab1-107">Costante</span><span class="sxs-lookup"><span data-stu-id="60ab1-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="60ab1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60ab1-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="60ab1-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-110">Ogni elemento nel controllo appare e si comporta come un pulsante di push.</span><span class="sxs-lookup"><span data-stu-id="60ab1-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="60ab1-111">Questo stile è utile se un'applicazione esegue un'attività quando l'utente fa clic su un elemento nel controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="60ab1-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="60ab1-112">Ad esempio, un'applicazione può ordinare le informazioni nelle colonne in modo diverso a seconda dell'elemento selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="60ab1-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="60ab1-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-114">Consente il riordinamento del trascinamento della selezione degli elementi di intestazione.</span><span class="sxs-lookup"><span data-stu-id="60ab1-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="60ab1-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-116">Includere una barra dei filtri come parte del controllo intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="60ab1-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="60ab1-117">Questa barra consente agli utenti di applicare comodamente un filtro alla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="60ab1-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="60ab1-118">Le chiamate a <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> produrranno nuove dimensioni per il controllo e comporteranno l'aggiornamento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="60ab1-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="60ab1-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-120"><a href="common-control-versions.md">Versione 6,0 e successive</a>.</span><span class="sxs-lookup"><span data-stu-id="60ab1-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="60ab1-121">Determina il disegno del controllo intestazione come flat quando il sistema operativo è in esecuzione in modalità classica.</span><span class="sxs-lookup"><span data-stu-id="60ab1-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="60ab1-122">Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows.</span><span class="sxs-lookup"><span data-stu-id="60ab1-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="60ab1-123">Per usare Comctl32.dll versione 6, specificarla in un manifesto.</span><span class="sxs-lookup"><span data-stu-id="60ab1-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="60ab1-124">Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="60ab1-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="60ab1-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-126">Consente al controllo intestazione di visualizzare il contenuto della colonna anche quando l'utente ridimensiona una colonna.</span><span class="sxs-lookup"><span data-stu-id="60ab1-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="60ab1-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-128">Indica un controllo intestazione che deve essere nascosto.</span><span class="sxs-lookup"><span data-stu-id="60ab1-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="60ab1-129">Questo stile non nasconde il controllo.</span><span class="sxs-lookup"><span data-stu-id="60ab1-129">This style does not hide the control.</span></span> <span data-ttu-id="60ab1-130">Al contrario, quando si invia il messaggio di <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> a un controllo intestazione con lo stile HDS_HIDDEN, il controllo restituisce zero nel membro <strong>CY</strong> della struttura <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60ab1-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="60ab1-131">Il controllo viene quindi nascosto impostando l'altezza su zero.</span><span class="sxs-lookup"><span data-stu-id="60ab1-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="60ab1-132">Questa operazione può essere utile quando si desidera utilizzare il controllo come contenitore di informazioni anziché come controllo visivo.</span><span class="sxs-lookup"><span data-stu-id="60ab1-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="60ab1-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-134">Crea un controllo intestazione con orientamento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="60ab1-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="60ab1-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-136">Abilita il rilevamento a caldo.</span><span class="sxs-lookup"><span data-stu-id="60ab1-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="60ab1-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-138"><a href="common-control-versions.md">Versione 6,00 e successive</a>.</span><span class="sxs-lookup"><span data-stu-id="60ab1-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="60ab1-139">Consente l'inserimento di caselle di controllo sugli elementi di intestazione.</span><span class="sxs-lookup"><span data-stu-id="60ab1-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="60ab1-140">Per ulteriori informazioni, vedere il membro <strong>FMT</strong> di <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60ab1-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="60ab1-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-142"><a href="common-control-versions.md">Versione 6,00 e successive</a>.</span><span class="sxs-lookup"><span data-stu-id="60ab1-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="60ab1-143">L'utente non può trascinare il divisore sul controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="60ab1-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="60ab1-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="60ab1-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="60ab1-145"><a href="common-control-versions.md">Versione 6,00 e successive</a>.</span><span class="sxs-lookup"><span data-stu-id="60ab1-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="60ab1-146">Quando non è possibile visualizzare tutti gli elementi all'interno del rettangolo del controllo intestazione, viene visualizzato un pulsante.</span><span class="sxs-lookup"><span data-stu-id="60ab1-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="60ab1-147">Quando si fa clic su questo pulsante, viene inviato un <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notifica.</span><span class="sxs-lookup"><span data-stu-id="60ab1-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="60ab1-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="60ab1-148">Remarks</span></span>

<span data-ttu-id="60ab1-149">Per recuperare e modificare gli stili dopo aver creato il controllo, usare le funzioni [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="60ab1-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ab1-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60ab1-150">Requirements</span></span>



| <span data-ttu-id="60ab1-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ab1-151">Requirement</span></span> | <span data-ttu-id="60ab1-152">Valore</span><span class="sxs-lookup"><span data-stu-id="60ab1-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60ab1-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60ab1-153">Header</span></span><br/> | <dl> <span data-ttu-id="60ab1-154"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ab1-154"><dt>CommCtrl.h</dt></span></span> </dl> |



