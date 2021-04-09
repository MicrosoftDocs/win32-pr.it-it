---
title: Windows (nozioni di base sulla progettazione)
description: Le finestre sono le principali \ 0034; Canvas \ 0034; o superfici dell'interfaccia utente dell'app desktop, incluse le finestre principali e i popup, le finestre di dialogo e le procedure guidate. Attenersi a queste linee guida per decidere quale superficie usare e come usarla.
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968827"
---
# <a name="windows-design-basics"></a><span data-ttu-id="d7399-104">Windows (nozioni di base sulla progettazione)</span><span class="sxs-lookup"><span data-stu-id="d7399-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="d7399-105">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="d7399-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="d7399-106">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="d7399-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="d7399-107">Windows sono i principali "canvas" o le superfici dell'interfaccia utente dell'app desktop, incluse le finestre principali e i popup, le finestre di dialogo e le procedure guidate.</span><span class="sxs-lookup"><span data-stu-id="d7399-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="d7399-108">Attenersi a queste linee guida per decidere quale superficie usare e come usarla.</span><span class="sxs-lookup"><span data-stu-id="d7399-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d7399-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d7399-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7399-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="d7399-110">Topic</span></span></th>
<th><span data-ttu-id="d7399-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7399-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7399-112"><a href="win-window-mgt.md">Gestione finestre</a></span><span class="sxs-lookup"><span data-stu-id="d7399-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="d7399-113">In questo articolo viene illustrata la posizione predefinita delle finestre quando visualizzate inizialmente sullo schermo, il relativo ordine di sovrapposizione rispetto ad altre finestre (<a href="glossary.md">z order</a>), le dimensioni iniziali e il modo in cui la visualizzazione influiscono sullo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="d7399-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7399-114"><a href="win-window-frames.md">Frame della finestra</a></span><span class="sxs-lookup"><span data-stu-id="d7399-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="d7399-115">La maggior parte dei programmi deve usare frame della finestra standard.</span><span class="sxs-lookup"><span data-stu-id="d7399-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="d7399-116">Le applicazioni immersive possono avere una modalità schermo intero che nasconde la cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="d7399-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="d7399-117">Prendere in considerazione l'uso di Glass in modo strategico per un aspetto più semplice, più chiaro e coeso.</span><span class="sxs-lookup"><span data-stu-id="d7399-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7399-118"><a href="win-dialog-box.md">Finestre di dialogo</a></span><span class="sxs-lookup"><span data-stu-id="d7399-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="d7399-119">Una finestra di dialogo è una finestra secondaria che consente agli utenti di eseguire un comando, chiedere agli utenti una domanda o fornire agli utenti informazioni o commenti e suggerimenti sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="d7399-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7399-120"><a href="win-common-dlg.md">Finestre di dialogo comuni</a></span><span class="sxs-lookup"><span data-stu-id="d7399-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="d7399-121">Le finestre di dialogo comuni di Microsoft Windows sono costituite dalle finestre di dialogo Apri file, Salva file, Apri cartella, trova e Sostituisci, stampa, Imposta pagina, carattere e colore.</span><span class="sxs-lookup"><span data-stu-id="d7399-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7399-122"><a href="win-wizards.md">Procedure guidate</a></span><span class="sxs-lookup"><span data-stu-id="d7399-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="d7399-123">Nonostante questo meraviglioso nome bizzarro, le procedure guidate non sono davvero una forma speciale di interfaccia utente e hanno solo una particolare gamma di utilità.</span><span class="sxs-lookup"><span data-stu-id="d7399-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7399-124"><a href="win-property-win.md">Finestre delle proprietà</a></span><span class="sxs-lookup"><span data-stu-id="d7399-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="d7399-125">La finestra delle proprietà è il nome collettivo per i tipi di interfacce utente (UI) seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7399-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="d7399-126">Finestra delle proprietà: utilizzata per <strong>visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in una</strong>finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d7399-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="d7399-127">Controllo proprietà: usato per <strong>visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in un riquadro</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7399-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="d7399-128">Finestra di dialogo Opzioni: consente di <strong>visualizzare e modificare le opzioni di un'applicazione</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7399-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

