---
description: Questa sezione contiene le proprietà per il controllo InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Proprietà InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759527"
---
# <a name="inkpicture-properties"></a>Proprietà InkPicture

Questa sezione contiene le proprietà per il controllo InkPicture.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Proprietà AutoRedraw</strong></a></td>
<td>Ottiene o imposta un valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> viene ridisegnato quando la finestra viene invalidata (se l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> attualmente associato al controllo InkPicture viene ridisegnato automaticamente quando la finestra associata a InkPicture riceve un messaggio di WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Ottiene o imposta il colore di sfondo per il controllo <a href="inkpicture-control-reference.md">InkPicture</a> . Il colore di sfondo predefinito è il colore di sfondo della finestra di sistema, in genere bianco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Proprietà CollectingInk</strong></a></td>
<td>Ottiene il valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> sta raccogliendo input penna (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o l'input penna e i movimenti vengono riconosciuti durante la scrittura da parte dell'utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors (proprietà)</strong></a></td>
<td>Ottiene la raccolta <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponibile per l'utilizzo nell'area Inking del controllo <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>Ottiene la raccolta <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> da salvare in modo permanente con l'input penna (solo in fase di progettazione).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Proprietà DefaultDrawingAttributes</strong></a></td>
<td>Ottiene o imposta la raccolta <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predefinita da utilizzare durante il disegno e la visualizzazione dell'input penna (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Proprietà DesiredPacketDescription</strong></a></td>
<td>Ottiene o imposta la descrizione del pacchetto del controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Proprietà DynamicRendering</strong></a></td>
<td>Ottiene o imposta il valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> esegue dinamicamente il rendering dell'input penna durante la raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Ottiene o imposta un valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> è in modalità input penna, modalità di eliminazione o selezione/modifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Abilitato</strong></a></td>
<td>Ottiene o imposta un valore che determina se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> può rispondere agli eventi generati dall'utente.<br/>
<blockquote>
[!Note]<br />
Questa proprietà è equivalente alla proprietà <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Ottiene o imposta il valore che specifica se l'input penna è stato cancellato dal tratto o dal punto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Ottiene o imposta il valore che specifica la larghezza della descrizione della penna della gomma.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></td>
<td>Ottiene l'handle della finestra a cui è associato il controllo <a href="inkpicture-control-reference.md">InkPicture</a> . (solo in fase di esecuzione)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Input penna</strong></a></td>
<td>Ottiene o imposta l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associato al controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Ottiene o imposta un valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> raccoglie l'input penna, ovvero i pacchetti in aria, il cursore negli eventi di intervallo e così via.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Proprietà MarginX</strong></a></td>
<td>Ottiene o imposta il margine dell'asse x intorno al rettangolo della finestra nelle coordinate dello schermo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Proprietà MarginY</strong></a></td>
<td>Ottiene o imposta il margine dell'asse y intorno al rettangolo della finestra nelle coordinate dello schermo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Proprietà MouseIcon</strong></a></td>
<td>Ottiene o imposta l'icona del mouse personalizzata corrente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Proprietà MousePointer</strong></a></td>
<td>Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Immagine</strong></a></td>
<td>Ottiene il file di grafica da visualizzare nel controllo <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (proprietà)</strong></a></td>
<td>Ottiene o imposta l'oggetto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> utilizzato per creare l'input penna nel controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selezione</strong></a></td>
<td>Ottiene la raccolta <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> attualmente selezionata all'interno del controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>Ottiene o imposta il modo in cui il controllo gestisce il posizionamento e il ridimensionamento delle immagini.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Proprietà SupportHighContrastInk</strong></a></td>
<td>Ottiene un valore che specifica se viene eseguito il rendering dell'input penna come un solo colore, color = COLOR_WINDOWTEXT (dalla chiamata GetSystemMetrics) quando il sistema è in modalità Contrasto elevato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Ottiene o imposta un valore che specifica se tutte le interfacce utente di selezione, ovvero i quadratini di selezione e gli handle di selezione, vengono disegnate con un contrasto elevato quando il sistema è in modalità Contrasto elevato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Proprietà Tablet</strong></a></td>
<td>Ottiene l'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> attualmente utilizzato dal controllo <a href="inkpicture-control-reference.md">InkPicture</a> per raccogliere input.<br/></td>
</tr>
</tbody>
</table>



 

