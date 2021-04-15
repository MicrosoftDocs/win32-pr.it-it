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
# <a name="using-tab-controls"></a>Uso di controlli struttura a schede

Questo argomento contiene due esempi che usano i controlli struttura a schede. Nel primo esempio viene illustrato come utilizzare un controllo struttura a schede per spostarsi tra più pagine di testo nella finestra principale di un'applicazione. Nel secondo esempio viene illustrato come utilizzare un controllo struttura a schede per spostarsi tra più pagine di controlli in una finestra di dialogo.

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
<td><a href="create-a-tab-control-in-the-main-window.md">Come creare un controllo struttura a schede nella finestra principale</a><br/></td>
<td>Nell'esempio riportato in questa sezione viene illustrato come creare un controllo struttura a schede e come visualizzarlo nell'area client della finestra principale dell'applicazione. Nell'applicazione viene visualizzata una terza finestra (un controllo statico) nell'area di visualizzazione del controllo struttura a schede. La finestra padre posiziona e ridimensiona il controllo struttura a schede e il controllo statico quando elabora il messaggio di <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> . <br/> In questo esempio sono presenti sette schede, una per ogni giorno della settimana. Quando l'utente seleziona una scheda, l'applicazione Visualizza il nome del giorno corrispondente nel controllo statico. <br/></td>
</tr>
<tr class="even">
<td><a href="create-a-tabbed-dialog-box.md">Come creare una finestra di dialogo a schede</a><br/></td>
<td>Nell'esempio riportato in questa sezione viene illustrato come creare una finestra di dialogo in cui vengono utilizzate schede per fornire più pagine di controlli. La finestra di dialogo principale è una finestra di dialogo modale. Ogni pagina di controlli è definita da un modello di finestra di dialogo con lo stile <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> . Quando si seleziona una scheda, viene creata una finestra di dialogo non modale per la pagina in ingresso e la finestra di dialogo per la pagina in uscita viene distrutta. <br/>
<blockquote>
[!Note]<br />
In molti casi, è possibile implementare più facilmente le finestre di dialogo a più pagine tramite le finestre delle proprietà. Per ulteriori informazioni sulle finestre delle proprietà, vedere <a href="property-sheets.md">informazioni sulle finestre delle proprietà</a>.
</blockquote>
<br/> Il modello per la finestra di dialogo principale definisce semplicemente due controlli Button. Quando si elabora il messaggio di <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , la routine della finestra di dialogo consente di creare un controllo struttura a schede e di caricare le risorse del modello della finestra di dialogo per ognuna delle finestre di dialogo figlio. <br/></td>
</tr>
</tbody>
</table>



 

