---
description: Il controllo InkPicture consente di inserire un'immagine in un'applicazione e consentire agli utenti di aggiungere input penna.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Riferimento al controllo InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8caaf1970394338f858cd0fdff0dab58153f53b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968611"
---
# <a name="inkpicture-control-reference"></a>Riferimento al controllo InkPicture

Il controllo InkPicture consente di inserire un'immagine in un'applicazione e consentire agli utenti di aggiungere input penna. È destinato agli scenari in cui l'input penna non è riconosciuto come testo ma viene invece archiviato come input penna.

È possibile creare un'istanza del controllo InkPicture chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

> [!Note]  
> Il controllo InkPicture non è contrassegnato come Safe per lo scripting. Il controllo InkPicture non deve essere utilizzato nelle pagine HTML o ASP.NET.

 

La creazione del controllo InkPicture dietro un controllo trasparente, ad esempio un GroupBox con il \_ set di proprietà WS ex \_ trasparente, impedisce a InkPicture di raccogliere input penna.

## <a name="members"></a>Membri



| Enumerazione                                      | Descrizione                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Definisce i valori che specificano il comportamento dell'immagine di sfondo all'interno del controllo InkPicture.<br/> |



 



| Event                                                                              | Descrizione                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Deprecato.<br/>                                                                                                                                                                                                                                                                                             |
| [**Clic**](inkpicture-click.md)                                                  | Si verifica quando un utente fa clic sul controllo InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)                      | Si verifica quando il controllo [**InkCollector**](inkcollector-class.md) rileva un oggetto [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) inattivo.<br/>                                                                                                                                                         |
| [**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)                          | Si verifica quando il controllo InkPicture rileva un [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) attivo.<br/>                                                                                                                                                                                                  |
| [**Evento CursorDown**](inkpicture-cursordown.md)                                  | Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.<br/>                                                                                                                                                                                                                                      |
| [**Evento CursorInRange**](inkpicture-cursorinrange.md)                            | Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.<br/>                                                                                                                                                                                                             |
| [**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)                      | Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.<br/>                                                                                                                                                                                                           |
| [**DblClick**](inkpicture-dblclick.md)                                            | Si verifica quando si fa doppio clic sul controllo InkPicture.<br/> Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** . L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IPEDblClick.<br/> |
| [**Evento movimento**](inkpicture-gesture.md)                                        | Si verifica quando viene riconosciuto un movimento dell'applicazione.<br/>                                                                                                                                                                                                                                                       |
| [**\[Controllo InkPicture evento KeyDown\]**](inkpicture-keydown.md)                 | Si verifica quando viene premuto un tasto e nella posizione in giù mentre il controllo InkPicture dispone dello stato attivo.<br/>                                                                                                                                                                                                           |
| [**\[Controllo InkPicture evento KeyPress\]**](inkpicture-keypress.md)                | Si verifica quando viene premuto un tasto mentre il controllo InkPicture dispone dello stato attivo.<br/>                                                                                                                                                                                                                                    |
| [**\[Controllo InkPicture evento KeyUp\]**](inkpicture-keyup.md)                     | Si verifica quando viene rilasciato un tasto mentre il controllo InkPicture dispone dello stato attivo.<br/>                                                                                                                                                                                                                                   |
| [**\[Controllo InkPicture evento MouseDown\]**](inkpicture-mousedown.md)             | Si verifica quando il puntatore del mouse si trova sul controllo InkPicture e viene premuto un pulsante del mouse.<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | Si verifica quando il puntatore del mouse entra nel controllo InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Si verifica quando il puntatore del mouse viene posizionato sul controllo InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Si verifica quando il puntatore del mouse esce dal controllo InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**\[Controllo InkPicture evento MouseMove\]**](inkpicture-mousemove.md)             | Si verifica quando il puntatore del mouse viene spostato sul controllo InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**\[Controllo InkPicture evento MouseUp\]**](inkpicture-mouseup.md)                 | Si verifica quando il puntatore del mouse si trova sul controllo InkPicture e viene rilasciato un pulsante del mouse.<br/>                                                                                                                                                                                                            |
| [**MouseWheel**](inkpicture-mousewheel.md)                                        | Si verifica quando viene spostata la rotellina del mouse mentre il controllo InkPicture dispone dello stato attivo.<br/>                                                                                                                                                                                                                               |
| [**Evento NewInAirPackets**](inkpicture-newinairpackets.md)                        | Si verifica quando viene visualizzato un pacchetto in aria.<br/>                                                                                                                                                                                                                                                                   |
| [**Evento NewPackets**](inkpicture-newpackets.md)                                  | Si verifica quando il controllo InkPicture riceve un pacchetto.<br/>                                                                                                                                                                                                                                                   |
| [**Dipinto**](inkpicture-painted.md)                                              | Si verifica quando il controllo InkPicture ha completato il ridisegno.<br/>                                                                                                                                                                                                                                      |
| [**Disegno**](inkpicture-painting.md)                                            | Si verifica prima che il controllo InkPicture venga ridisegnato.<br/>                                                                                                                                                                                                                                                    |
| [**Ridimensionamento**](inkpicture-resize.md)                                                | Si verifica quando il controllo InkPicture viene ridimensionato.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Si verifica quando la selezione del testo all'interno del controllo InkPicture viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                    |
| [**SelectionChanging**](inkpicture-selectionchanging.md)                          | Si verifica quando la selezione del testo all'interno del controllo InkPicture sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                  |
| [**\[Controllo InkPicture evento SelectionMoving\]**](inkpicture-selectionmoving.md) | Si verifica quando la posizione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Si verifica quando la dimensione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                      |
| [**SelectionResizing**](inkpicture-selectionresizing.md)                          | Si verifica quando la dimensione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Si verifica dopo che il controllo InkPicture è stato ridimensionato, in particolare, dopo la modifica del valore della proprietà [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Si verifica dopo la modifica della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del controllo InkPicture.<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | Non implementato.<br/>                                                                                                                                                                                                                                                                                        |
| [**Stroke**](inkpicture-stroke.md)                                                | Si verifica quando l'utente disegna un nuovo tratto su un tablet.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Si verifica dopo l'eliminazione degli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Si verifica prima dell'eliminazione degli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Si verifica dopo la modifica dei colori di sistema.<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | Si verifica quando viene riconosciuto un movimento del sistema.<br/>                                                                                                                                                                                                                                                             |
| [**Evento TabletAdded**](inkpicture-tabletadded.md)                                | Si verifica quando un tablet viene aggiunto al sistema.<br/>                                                                                                                                                                                                                                                            |
| [**Evento TabletRemoved**](inkpicture-tabletremoved.md)                            | Si verifica quando un tablet viene rimosso dal sistema.<br/>                                                                                                                                                                                                                                                        |



 



| Metodo                                                                                   | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Restituisce un valore che indica se il controllo InkPicture è interessato da un particolare evento.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Restituisce un valore che indica se il controllo InkPicture è interessato da un particolare movimento dell'applicazione.<br/>                                                     |
| [**Metodo GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Restituisce il rettangolo della finestra, in pixel, all'interno del quale viene disegnato l'input penna.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Restituisce un membro dell'enumerazione [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , che specifica quale parte di una selezione, se presente, è stata raggiunta durante un hit test.<br/> |
| [**Metodo SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Consente al controllo InkPicture di raccogliere input penna da qualsiasi tablet collegato al Tablet PC.<br/>                                                                            |
| [**Metodo SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Imposta un valore che indica se un controllo InkPicture è interessato a un evento specificato.<br/>                                                                        |
| SetFocus                                                                                 | Sposta lo stato attivo sul controllo InkPicture.<br/>                                                                                                                          |
| [**Metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Imposta l'interesse dell'oggetto InkPicture in un movimento dell'applicazione specificato.<br/>                                                                                      |
| [**Metodo SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Imposta il controllo InkPicture per la raccolta di input penna da un solo tablet collegato al Tablet PC. L'input penna da altre tavolette viene ignorato.<br/>                                       |
| [**Metodo SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Specifica il rettangolo della finestra da impostare, nelle coordinate della finestra, all'interno del quale viene disegnato l'input penna.<br/>                                                                            |
| ShowWhatsThis                                                                            | Visualizza un argomento selezionato in un file della Guida utilizzando il popup "What ' s this" fornito dalla guida nei sistemi operativi Microsoft Windows a 32 bit (solo in fase di progettazione).<br/>           |
| ZOrder                                                                                   | Posiziona il controllo nella parte anteriore o posteriore dell'ordine z all'interno del relativo livello grafico (solo in fase di progettazione).<br/>                                                               |



 



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
<td>Ottiene o imposta un valore che specifica se il controllo InkPicture viene ridisegnato quando la finestra viene invalidata (se l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> attualmente associato al controllo InkPicture viene ridisegnato automaticamente quando la finestra associata a InkPicture riceve un messaggio di WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Ottiene o imposta il colore di sfondo per il controllo InkPicture. Il colore di sfondo predefinito è il colore di sfondo della finestra di sistema, in genere bianco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Proprietà CollectingInk</strong></a></td>
<td>Ottiene il valore che specifica se il controllo InkPicture sta raccogliendo input penna (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o l'input penna e i movimenti vengono riconosciuti durante la scrittura da parte dell'utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors (proprietà)</strong></a></td>
<td>Ottiene la raccolta <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponibile per l'utilizzo nell'area Inking del controllo InkPicture.<br/></td>
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
<td>Ottiene o imposta la descrizione del pacchetto del controllo InkPicture (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Proprietà DynamicRendering</strong></a></td>
<td>Ottiene o imposta il valore che specifica se il controllo InkPicture esegue dinamicamente il rendering dell'input penna durante la raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Ottiene o imposta un valore che specifica se il controllo InkPicture è in modalità input penna, modalità di eliminazione o selezione/modifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Abilitato</strong></a></td>
<td>Ottiene o imposta un valore che determina se il controllo InkPicture può rispondere agli eventi generati dall'utente.<br/>
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
<td>Ottiene l'handle della finestra a cui è associato il controllo InkPicture. (solo in fase di esecuzione)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Input penna</strong></a></td>
<td>Ottiene o imposta l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associato al controllo InkPicture (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Ottiene o imposta un valore che specifica se il controllo InkPicture raccoglie l'input penna, ovvero i pacchetti in aria, il cursore negli eventi di intervallo e così via.<br/></td>
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
<td>Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo InkPicture.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Immagine</strong></a></td>
<td>Ottiene il file di grafica da visualizzare nel controllo InkPicture.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (proprietà)</strong></a></td>
<td>Ottiene o imposta l'oggetto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> utilizzato per creare l'input penna nel controllo InkPicture (solo in fase di esecuzione).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selezione</strong></a></td>
<td>Ottiene la raccolta <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> attualmente selezionata all'interno del controllo InkPicture (solo in fase di esecuzione).<br/></td>
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
<td>Ottiene l'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> attualmente utilizzato dal controllo InkPicture per raccogliere input.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

L'interfaccia utente di run-time per il controllo InkPicture è una finestra con uno sfondo opaco (a colore singolo, sfondo immagine o entrambi) che contiene un input penna opaco.

È possibile utilizzare il controllo InkPicture per eseguire il rendering dell'input penna in Microsoft Windows 2000, Windows Server 2003, qualsiasi edizione di Windows XP diversa da Windows XP Tablet PC Edition e qualsiasi versione di Windows Vista. Tuttavia, è possibile immettere input penna, accettare movimenti o riconoscere la grafia solo nelle condizioni seguenti:

-   L'input penna può essere inserito e riconosciuto se è installato Windows Vista o XP Tablet PC Edition 2005.
-   I movimenti possono anche essere riconosciuti.
-   La grafia può essere riconosciuta come testo se la grafia è stata originata nei computer che eseguono versioni precedenti di Windows, purché siano presenti i riconoscitori.

Se si utilizza Windows 2000, Windows Server 2003, qualsiasi edizione di Windows XP diversa da Windows XP Tablet PC Edition 2005, è possibile assegnare i valori alle proprietà di ambiente del controllo InkPicture, quindi copiare e incollare l'input penna in altre applicazioni. Tuttavia, il valore della proprietà InkEnabled sarà sempre **false**.

Gli oggetti [**InkDisp**](inkdisp-class.md) salvati in forma permanente possono essere caricati e visualizzati in tutte le edizioni di Windows Vista e XP e nei sistemi in cui è installato solo Windows XP Tablet PC Edition Software Development Kit (SDK). Gli oggetti **InkDisp** possono essere convertiti solo in testo (riconosciuto), se è installato Windows Vista o Windows XP Tablet PC Edition 2005.

Se le operazioni eseguite su questo controllo non hanno esito positivo, viene restituito un HRESULT valido. Se le condizioni di errore risultano, controllare il valore HRESULT restituito a fronte dell'errore.

Per ulteriori informazioni sui controlli Ink, vedere [input penna](ink-controls.md).

Per informazioni sui thread che generano eventi specifici, vedere [thread sui quali è possibile attivare un evento](threads-on-which-an-event-can-fire.md).

Per migliorare le prestazioni dell'applicazione, eliminare manualmente un controllo InkPicture quando non è più necessario.

> [!Note]  
> Quando un controllo InkPicture viene sovrapposto a un altro controllo, ad esempio un oggetto **GroupBox** impostato su Transparent, InkPicture non raccoglierà l'input penna. InkPicture deve essere il controllo di primo livello nell'ordine Z oppure deve essere un elemento figlio del **GroupBox**.

 

## <a name="com-implementation"></a>Implementazione COM

Questo oggetto implementa l'interfaccia com **IInkPicture** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> </dl>

