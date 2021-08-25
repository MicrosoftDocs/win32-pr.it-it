---
description: Il controllo InkPicture consente di posizionare un'immagine in un'applicazione e consentire agli utenti di aggiungere input penna.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Informazioni di riferimento sul controllo InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93f5727d2f3f049a579e32e5feb0ba0eaa742d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471537"
---
# <a name="inkpicture-control-reference"></a>Informazioni di riferimento sul controllo InkPicture

Il controllo InkPicture consente di posizionare un'immagine in un'applicazione e consentire agli utenti di aggiungere input penna. È destinato a scenari in cui l'input penna non viene riconosciuto come testo, ma viene invece archiviato come input penna.

È possibile creare un'istanza del controllo InkPicture chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

> [!Note]  
> Il controllo InkPicture non è contrassegnato come sicuro per lo scripting. Il controllo InkPicture non deve essere usato in HTML o ASP.NET pagine.

 

La creazione del controllo InkPicture dietro un controllo trasparente (ad esempio un controllo GroupBox con il set di proprietà WS EX TRANSPARENT) impedirà a InkPicture di raccogliere input \_ \_ penna.

## <a name="members"></a>Membri



| Enumerazione                                      | Descrizione                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Definisce valori che specificano il comportamento dell'immagine di sfondo all'interno del controllo InkPicture.<br/> |



 



| Event                                                                              | Descrizione                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Deprecato.<br/>                                                                                                                                                                                                                                                                                             |
| [**Clic**](inkpicture-click.md)                                                  | Si verifica quando un utente fa clic sul controllo InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)                      | Si verifica quando [**il controllo InkCollector**](inkcollector-class.md) rileva un [**oggetto IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) non disponibile.<br/>                                                                                                                                                         |
| [**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)                          | Si verifica quando il controllo InkPicture rileva un [**controllo IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) in stato di insoddizione.<br/>                                                                                                                                                                                                  |
| [**Evento CursorDown**](inkpicture-cursordown.md)                                  | Si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.<br/>                                                                                                                                                                                                                                      |
| [**Evento CursorInRange**](inkpicture-cursorinrange.md)                            | Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto del tablet.<br/>                                                                                                                                                                                                             |
| [**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)                      | Si verifica quando il cursore lascia l'intervallo di rilevamento fisico (prossimità) del contesto del tablet.<br/>                                                                                                                                                                                                           |
| [**Dblclick**](inkpicture-dblclick.md)                                            | Si verifica quando si fa doppio clic sul controllo InkPicture.<br/> Questo metodo di evento è definito **\_ nell'interfaccia IInkPictureEvents.** **\_ L'interfaccia IInkPictureEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore \_ DISPID IPEDblClick.<br/> |
| [**Evento movimento**](inkpicture-gesture.md)                                        | Si verifica quando viene riconosciuto un movimento dell'applicazione.<br/>                                                                                                                                                                                                                                                       |
| [**Controllo \[ InkPicture dell'evento KeyDown\]**](inkpicture-keydown.md)                 | Si verifica quando viene premuto un tasto e nella posizione verso il basso mentre il controllo InkPicture ha lo stato attivo.<br/>                                                                                                                                                                                                           |
| [**Controllo \[ InkPicture dell'evento KeyPress\]**](inkpicture-keypress.md)                | Si verifica quando viene premuto un tasto mentre il controllo InkPicture ha lo stato attivo.<br/>                                                                                                                                                                                                                                    |
| [**Controllo \[ InkPicture dell'evento KeyUp\]**](inkpicture-keyup.md)                     | Si verifica quando viene rilasciato un tasto mentre il controllo InkPicture ha lo stato attivo.<br/>                                                                                                                                                                                                                                   |
| [**Controllo \[ InkPicture dell'evento MouseDown\]**](inkpicture-mousedown.md)             | Si verifica quando il puntatore del mouse è posizionato sul controllo InkPicture e viene premuto un pulsante del mouse.<br/>                                                                                                                                                                                                             |
| [**Mouseenter**](inkpicture-mouseenter.md)                                        | Si verifica quando il puntatore del mouse entra nel controllo InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Si verifica quando il puntatore del mouse viene posizionato sul controllo InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**Mouseleave**](inkpicture-mouseleave.md)                                        | Si verifica quando il puntatore del mouse esce dal controllo InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**Controllo \[ InkPicture dell'evento MouseMove\]**](inkpicture-mousemove.md)             | Si verifica quando il puntatore del mouse viene spostato sul controllo InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**Controllo \[ InkPicture dell'evento MouseUp\]**](inkpicture-mouseup.md)                 | Si verifica quando il puntatore del mouse viene posizionato sul controllo InkPicture e viene rilasciato un pulsante del mouse.<br/>                                                                                                                                                                                                            |
| [**Mousewheel**](inkpicture-mousewheel.md)                                        | Si verifica quando la rotellina del mouse si sposta mentre il controllo InkPicture ha lo stato attivo.<br/>                                                                                                                                                                                                                               |
| [**Evento NewInAirPackets**](inkpicture-newinairpackets.md)                        | Si verifica quando viene visualizzato un pacchetto in aria.<br/>                                                                                                                                                                                                                                                                   |
| [**Evento NewPackets**](inkpicture-newpackets.md)                                  | Si verifica quando il controllo InkPicture riceve un pacchetto.<br/>                                                                                                                                                                                                                                                   |
| [**Dipinto**](inkpicture-painted.md)                                              | Si verifica quando il controllo InkPicture ha completato il ridisegno stesso.<br/>                                                                                                                                                                                                                                      |
| [**Pittura**](inkpicture-painting.md)                                            | Si verifica prima che il controllo InkPicture ridisegni se stesso.<br/>                                                                                                                                                                                                                                                    |
| [**Ridimensionamento**](inkpicture-resize.md)                                                | Si verifica quando il controllo InkPicture viene ridimensionato.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Si verifica quando la selezione di testo all'interno del controllo InkPicture viene modificata, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                    |
| [**Selectionchanging**](inkpicture-selectionchanging.md)                          | Si verifica quando la selezione di testo all'interno del controllo InkPicture sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o alla [**proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | Si verifica quando la posizione della selezione corrente è stata modificata, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                                  |
| [**Controllo \[ InkPicture dell'evento SelectionMoving\]**](inkpicture-selectionmoving.md) | Si verifica quando la posizione della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Si verifica quando le dimensioni della selezione corrente sono cambiate, ad esempio tramite modifiche all'interfaccia utente, alle procedure taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                                      |
| [**Selectionresizing**](inkpicture-selectionresizing.md)                          | Si verifica quando le dimensioni della selezione corrente sta per cambiare, ad esempio tramite modifiche all'interfaccia utente, alle procedure di taglia e incolla o [**alla proprietà Selection.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)<br/>                                                                                               |
| [**Sizechanged**](inkpicture-sizechanged.md)                                      | Si verifica dopo il ridimensionamento del controllo InkPicture, in particolare dopo la modifica del valore della proprietà [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | Si verifica dopo la modifica della proprietà [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del controllo InkPicture.<br/>                                                                                                                                                                                           |
| **Stylechanged**                                                                   | Non implementato.<br/>                                                                                                                                                                                                                                                                                        |
| [**Infarto**](inkpicture-stroke.md)                                                | Si verifica quando l'utente disegna un nuovo tratto su qualsiasi tablet.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Si verifica [**dopo l'eliminazione di oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla [**proprietà Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Si verifica [**prima dell'eliminazione degli oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dalla [**proprietà Ink.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Si verifica dopo la modifica dei colori di sistema.<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | Si verifica quando viene riconosciuto un movimento di sistema.<br/>                                                                                                                                                                                                                                                             |
| [**Evento TabletAdded**](inkpicture-tabletadded.md)                                | Si verifica quando un tablet viene aggiunto al sistema.<br/>                                                                                                                                                                                                                                                            |
| [**Evento TabletRemoved**](inkpicture-tabletremoved.md)                            | Si verifica quando un tablet viene rimosso dal sistema.<br/>                                                                                                                                                                                                                                                        |



 



| Metodo                                                                                   | Descrizione                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Restituisce un valore che indica se il controllo InkPicture è interessato a un evento specifico.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Restituisce un valore che indica se il controllo InkPicture è interessato a un particolare movimento dell'applicazione.<br/>                                                     |
| [**Metodo GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Restituisce il rettangolo della finestra, in pixel, all'interno del quale viene disegnato l'input penna.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Restituisce un membro [**dell'enumerazione SelectionHitResult,**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) che specifica quale parte di una selezione, se presente, è stata raggiunto durante un hit test.<br/> |
| [**Metodo SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Consente al controllo InkPicture di raccogliere input penna da qualsiasi tablet collegato al Tablet PC.<br/>                                                                            |
| [**Metodo SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Imposta un valore che indica se un controllo InkPicture è interessato a un evento specificato.<br/>                                                                        |
| SetFocus                                                                                 | Sposta lo stato attivo sul controllo InkPicture.<br/>                                                                                                                          |
| [**Metodo SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Imposta l'interesse dell'oggetto InkPicture in un movimento dell'applicazione specificato.<br/>                                                                                      |
| [**Metodo SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Imposta il controllo InkPicture per raccogliere input penna da un solo tablet collegato al Tablet PC. L'input penna di altre tablet viene ignorato.<br/>                                       |
| [**Metodo SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Specifica il rettangolo della finestra da impostare, in coordinate della finestra, all'interno del quale viene disegnato l'input penna.<br/>                                                                            |
| ShowWhatsThis                                                                            | Visualizza un argomento selezionato in un file della Guida usando la finestra popup "What's This" fornita dalla Guida nei sistemi operativi Microsoft Windows a 32 bit (solo in fase di progettazione).<br/>           |
| Zorder                                                                                   | Posiziona il controllo all'inizio o alla fine dell'ordine Z all'interno del relativo livello grafico (solo in fase di progettazione).<br/>                                                               |



 




| Proprietà | Descrizione | 
|----------|-------------|
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Proprietà AutoRedraw</strong></a> | Ottiene o imposta un valore che specifica se il controllo InkPicture viene ridisegnato quando la finestra viene invalidata (se l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> attualmente associato al controllo InkPicture viene ridisegnato automaticamente quando la finestra associata a InkPicture riceve un messaggio WM_PAINT).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Backcolor</strong></a> | Ottiene o imposta il colore di sfondo per il controllo InkPicture. Il colore di sfondo predefinito è il colore di sfondo della finestra di sistema, in genere bianco.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Proprietà CollectingInk</strong></a> | Ottiene il valore che specifica se il controllo InkPicture sta raccogliendo input penna (solo in fase di esecuzione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a> | Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o l'input penna e i movimenti vengono riconosciuti durante la scrittura da parte dell'utente.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Proprietà Cursors</strong></a> | Ottiene la <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>raccolta IInkCursors</strong></a> disponibile per l'uso nell'area di input penna del controllo InkPicture.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>Sequenze personalizzate</strong></a> | Ottiene la <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>raccolta IInkCustomStrokes</strong></a> da rendere persistente con l'input penna (solo in fase di progettazione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Proprietà DefaultDrawingAttributes</strong></a> | Ottiene o imposta la raccolta <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predefinita da usare per disegnare e visualizzare input penna (solo in fase di esecuzione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Proprietà DesiredPacketDescription</strong></a> | Ottiene o imposta la descrizione del pacchetto del controllo InkPicture (solo in fase di esecuzione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Proprietà DynamicRendering</strong></a> | Ottiene o imposta il valore che specifica se il controllo InkPicture esegue dinamicamente il rendering dell'input penna durante la raccolta.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>Modalità di modifica</strong></a> | Ottiene o imposta un valore che specifica se il controllo InkPicture è in modalità input penna, in modalità di eliminazione o in modalità di selezione/modifica.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Attivato</strong></a> | Ottiene o imposta un valore che determina se il controllo InkPicture può rispondere agli eventi generati dall'utente.<br /><blockquote>[!Note]<br />Questa proprietà equivale alla <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>proprietà InkEnabled.</strong></a></blockquote><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a> | Ottiene o imposta il valore che specifica se l'input penna viene cancellato in base al tratto o al punto.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a> | Ottiene o imposta il valore che specifica la larghezza della punta della penna della gomma.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Hwnd</strong></a> | Ottiene l'handle di finestra a cui è associato il controllo InkPicture. (solo in fase di esecuzione)<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Input penna</strong></a> | Ottiene o imposta <a href="inkdisp-class.md"><strong>l'oggetto InkDisp</strong></a> associato al controllo InkPicture (solo in fase di esecuzione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> | Ottiene o imposta un valore che specifica se il controllo InkPicture raccoglie l'input penna (pacchetti in aria, cursore in eventi di intervallo e così via).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Proprietà MarginX</strong></a> | Ottiene o imposta il margine dell'asse x intorno al rettangolo della finestra nelle coordinate dello schermo.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Proprietà MarginY</strong></a> | Ottiene o imposta il margine dell'asse y intorno al rettangolo della finestra nelle coordinate dello schermo.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Proprietà MouseIcon</strong></a> | Ottiene o imposta l'icona del mouse personalizzata corrente.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Proprietà MousePointer</strong></a> | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Immagine</strong></a> | Ottiene il file di grafica da visualizzare nel controllo InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Proprietà Renderer</strong></a> | Ottiene o imposta <a href="inkrenderer-class.md"><strong>l'oggetto InkRenderer</strong></a> usato per disegnare input penna sul controllo InkPicture (solo in fase di esecuzione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selezione</strong></a> | Ottiene la <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">raccolta InkStrokes</a> attualmente selezionata all'interno del controllo InkPicture (solo in fase di esecuzione).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a> | Ottiene o imposta il modo in cui il controllo gestisce il posizionamento e il ridimensionamento delle immagini.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Proprietà SupportHighContrastInk</strong></a> | Ottiene un valore che specifica se viene eseguito il rendering dell'input penna come un solo colore, Color = COLOR_WINDOWTEXT (dalla chiamata a GetSystemMetrics) quando il sistema è in Contrasto elevato predefinita.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a> | Ottiene o imposta un valore che specifica se tutte le interfacce utente di selezione (rettangolo di selezione e quadratini di selezione) vengono disegnate in contrasto elevato quando il sistema è in Contrasto elevato modalità.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Proprietà Tablet</strong></a> | Ottiene <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>l'oggetto IInkTablet</strong></a> attualmente utilizzato dal controllo InkPicture per raccogliere l'input.<br /> | 




 

## <a name="remarks"></a>Commenti

L'interfaccia utente della fase di esecuzione per il controllo InkPicture è una finestra con uno sfondo opaco (a colore singolo, sfondo immagine o entrambi) che contiene input penna opaco.

È possibile usare il controllo InkPicture per eseguire il rendering dell'input penna in Microsoft Windows 2000, Windows Server 2003, in qualsiasi edizione di Windows XP diversa da Windows XP Tablet PC Edition e in qualsiasi versione di Windows Vista. È tuttavia possibile immettere input penna, accettare movimenti o riconoscere la grafia solo nelle condizioni seguenti:

-   L'input penna può essere immesso e riconosciuto se Windows Vista o XP Tablet PC Edition 2005 è installato.
-   Anche i movimenti possono essere riconosciuti.
-   La grafia può essere riconosciuta come testo se la grafia ha avuto origine in computer che eseguono versioni precedenti di Windows purché siano presenti riconoscitori.

Se si usa Windows 2000, Windows Server 2003, qualsiasi edizione di Windows XP diversa da Windows XP Tablet PC Edition 2005, è possibile assegnare valori alle proprietà di ambiente del controllo InkPicture, quindi copiare e incollare input penna in altre applicazioni. Tuttavia, il valore della relativa proprietà InkEnabled sarà sempre **FALSE.**

Gli oggetti [**InkDisp**](inkdisp-class.md) persistenti possono essere caricati e visualizzati in tutte le edizioni di Windows Vista e XP e nei sistemi in cui è installato solo Windows XP Tablet PC Edition Software Development Kit (SDK). **Gli oggetti InkDisp** possono essere convertiti solo in testo (riconosciuto), se Windows Vista o Windows XP Tablet PC Edition 2005 è installato.

Se le operazioni su questo controllo non hanno esito positivo, viene restituito un HRESULT valido. Se si verificano condizioni di errore, controllare il valore HRESULT restituito rispetto all'errore.

Per altre informazioni sui controlli input penna, vedere [Ink.](ink-controls.md)

Per informazioni sui thread che generano eventi specifici, vedere [Thread in cui può essere generato un evento.](threads-on-which-an-event-can-fire.md)

Per migliorare le prestazioni dell'applicazione, eliminare manualmente un controllo InkPicture quando non è più necessario.

> [!Note]  
> Quando un controllo InkPicture viene sovrapposto a un altro controllo, ad esempio **un oggetto GroupBox** impostato su transparent, InkPicture non raccoglie l'input penna. InkPicture deve essere il controllo più in alto nell'ordine Z o deve essere un elemento figlio di **GroupBox.**

 

## <a name="com-implementation"></a>Implementazione COM

Questo oggetto implementa **l'interfaccia COM IInkPicture.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul controllo InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> </dl>

