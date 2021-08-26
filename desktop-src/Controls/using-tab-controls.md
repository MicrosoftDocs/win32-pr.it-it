---
title: Uso dei controlli Struttura a schede
description: Questo argomento contiene due esempi che usano i controlli Struttura a schede.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbefde4b067c64fbdc66d7308bcb801c4fa504222168bb3436f7fbd69229706f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059381"
---
# <a name="using-tab-controls"></a>Uso dei controlli Struttura a schede

Questo argomento contiene due esempi che usano i controlli Struttura a schede. Nel primo esempio viene illustrato come usare un controllo Struttura a schede per spostarsi tra più pagine di testo nella finestra principale di un'applicazione. Nel secondo esempio viene illustrato come usare un controllo Struttura a schede per spostarsi tra più pagine di controlli in una finestra di dialogo.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-a-tab-control-in-the-main-window.md">Come creare un controllo Struttura a schede nella finestra principale</a><br/></td>
<td>L'esempio in questa sezione illustra come creare un controllo Struttura a schede e visualizzarlo nell'area client della finestra principale dell'applicazione. L'applicazione visualizza una terza finestra (un controllo statico) nell'area di visualizzazione del controllo Struttura a schede. La finestra padre posiziona e ridimensiona il controllo Struttura a schede e il controllo statico quando elabora il <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> messaggio. <br/> In questo esempio sono presenti sette schede, una per ogni giorno della settimana. Quando l'utente seleziona una scheda, l'applicazione visualizza il nome del giorno corrispondente nel controllo statico. <br/></td>
</tr>
<tr class="even">
<td><a href="create-a-tabbed-dialog-box.md">Come creare una finestra di dialogo a schede</a><br/></td>
<td>L'esempio in questa sezione illustra come creare una finestra di dialogo che usa schede per fornire più pagine di controlli. La finestra di dialogo principale è una finestra di dialogo modale. Ogni pagina di controlli è definita da un modello di finestra di dialogo con lo <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> personalizzato. Quando si seleziona una scheda, viene creata una finestra di dialogo non modabile per la pagina in ingresso e la finestra di dialogo per la pagina in uscita viene distrutta. <br/>
<blockquote>
[!Note]<br />
In molti casi, è possibile implementare più facilmente finestre di dialogo a più pagine usando le finestre delle proprietà. Per altre informazioni sulle finestre delle proprietà, vedere <a href="property-sheets.md">Informazioni sulle finestre delle proprietà.</a>
</blockquote>
<br/> Il modello per la finestra di dialogo principale definisce semplicemente due controlli pulsante. Quando si elabora <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>il WM_INITDIALOG,</strong></a> la routine della finestra di dialogo crea un controllo Struttura a schede e carica le risorse del modello di finestra di dialogo per ognuna delle finestre di dialogo figlio. <br/></td>
</tr>
</tbody>
</table>



 

