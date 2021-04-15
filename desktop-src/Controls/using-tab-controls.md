---
title: Uso di controlli struttura a schede
description: Questo argomento contiene due esempi che usano i controlli struttura a schede.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474510"
---
# <a name="using-tab-controls"></a><span data-ttu-id="53124-103">Uso di controlli struttura a schede</span><span class="sxs-lookup"><span data-stu-id="53124-103">Using Tab Controls</span></span>

<span data-ttu-id="53124-104">Questo argomento contiene due esempi che usano i controlli struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="53124-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="53124-105">Nel primo esempio viene illustrato come utilizzare un controllo struttura a schede per spostarsi tra più pagine di testo nella finestra principale di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53124-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="53124-106">Nel secondo esempio viene illustrato come utilizzare un controllo struttura a schede per spostarsi tra più pagine di controlli in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="53124-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53124-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="53124-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53124-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="53124-108">Topic</span></span></th>
<th><span data-ttu-id="53124-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53124-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53124-110"><a href="create-a-tab-control-in-the-main-window.md">Come creare un controllo struttura a schede nella finestra principale</a></span><span class="sxs-lookup"><span data-stu-id="53124-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="53124-111">Nell'esempio riportato in questa sezione viene illustrato come creare un controllo struttura a schede e come visualizzarlo nell'area client della finestra principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53124-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="53124-112">Nell'applicazione viene visualizzata una terza finestra (un controllo statico) nell'area di visualizzazione del controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="53124-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="53124-113">La finestra padre posiziona e ridimensiona il controllo struttura a schede e il controllo statico quando elabora il messaggio di <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="53124-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="53124-114">In questo esempio sono presenti sette schede, una per ogni giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="53124-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="53124-115">Quando l'utente seleziona una scheda, l'applicazione Visualizza il nome del giorno corrispondente nel controllo statico.</span><span class="sxs-lookup"><span data-stu-id="53124-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53124-116"><a href="create-a-tabbed-dialog-box.md">Come creare una finestra di dialogo a schede</a></span><span class="sxs-lookup"><span data-stu-id="53124-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="53124-117">Nell'esempio riportato in questa sezione viene illustrato come creare una finestra di dialogo in cui vengono utilizzate schede per fornire più pagine di controlli.</span><span class="sxs-lookup"><span data-stu-id="53124-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="53124-118">La finestra di dialogo principale è una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="53124-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="53124-119">Ogni pagina di controlli è definita da un modello di finestra di dialogo con lo stile <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="53124-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="53124-120">Quando si seleziona una scheda, viene creata una finestra di dialogo non modale per la pagina in ingresso e la finestra di dialogo per la pagina in uscita viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="53124-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="53124-121">In molti casi, è possibile implementare più facilmente le finestre di dialogo a più pagine tramite le finestre delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="53124-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="53124-122">Per ulteriori informazioni sulle finestre delle proprietà, vedere <a href="property-sheets.md">informazioni sulle finestre delle proprietà</a>.</span><span class="sxs-lookup"><span data-stu-id="53124-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="53124-123">Il modello per la finestra di dialogo principale definisce semplicemente due controlli Button.</span><span class="sxs-lookup"><span data-stu-id="53124-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="53124-124">Quando si elabora il messaggio di <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , la routine della finestra di dialogo consente di creare un controllo struttura a schede e di caricare le risorse del modello della finestra di dialogo per ognuna delle finestre di dialogo figlio.</span><span class="sxs-lookup"><span data-stu-id="53124-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

