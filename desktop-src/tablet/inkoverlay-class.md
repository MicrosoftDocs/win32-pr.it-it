---
description: Rappresenta un oggetto utile per gli scenari di annotazione in cui gli utenti non sono interessati a eseguire il riconoscimento sull'input penna ma sono interessati alla dimensione, alla forma, al colore e alla posizione dell'input penna.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: Classe InkOverlay (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: bfcc6cc4daedf0ed1bbc43e2ccc78317f9d7e17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313937"
---
# <a name="inkoverlay-class"></a>InkOverlay (classe)

Rappresenta un oggetto utile per gli scenari di annotazione in cui gli utenti non sono interessati a eseguire il riconoscimento sull'input penna ma sono interessati alla dimensione, alla forma, al colore e alla posizione dell'input penna.

La creazione del controllo **InkOverlay** dietro un controllo trasparente, ad esempio un GroupBox con il \_ set di proprietà WS ex \_ trasparente, impedisce a **InkOverlay** di raccogliere input penna.

**InkOverlay** presenta questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La classe **InkOverlay** presenta questi eventi.



| Event                                                     | Descrizione                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Si verifica quando l'oggetto **InkOverlay** rileva un pulsante del cursore inattivo.<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Si verifica quando l'oggetto **InkOverlay** rileva un pulsante del cursore che è attivo.<br/>                                                                                                                                                                             |
| [**CursorDown**](inkcollector-cursordown.md)             | Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.<br/>                                                                                                                                                                             |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.<br/>                                                                                                                                                    |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.<br/>                                                                                                                                                  |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Si verifica quando si fa doppio clic sull'oggetto **InkOverlay** .<br/>                                                                                                                                                                                       |
| [**Movimento**](inkcollector-gesture.md)                   | Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.<br/>                                                                                                                                                                                     |
| [**MouseDown**](inkcollector-mousedown.md)               | Si verifica quando il puntatore del mouse si trova sull'oggetto **InkOverlay** e viene premuto un pulsante del mouse.<br/>                                                                                                                                                 |
| [**MouseMove**](inkcollector-mousemove.md)               | Si verifica quando il puntatore del mouse viene spostato sull'oggetto **InkOverlay** .<br/>                                                                                                                                                                         |
| [**MouseUp**](inkcollector-mouseup.md)                   | Si verifica quando il puntatore del mouse si trova sull'oggetto **InkOverlay** e viene rilasciato un pulsante del mouse.<br/>                                                                                                                                                |
| [**MouseWheel**](inkcollector-mousewheel.md)             | Si verifica quando viene spostata la rotellina del mouse mentre l'oggetto **InkOverlay** dispone dello stato attivo.<br/>                                                                                                                                                                   |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Si verifica quando viene rilevato un pacchetto in aria, che si verifica quando un utente sposta una penna accanto al tablet e il cursore si trova all'interno della finestra dell'oggetto **InkOverlay** oppure l'utente sposta il mouse all'interno della finestra associata dell'oggetto **InkOverlay** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Si verifica quando l'oggetto **InkOverlay** riceve i pacchetti.<br/>                                                                                                                                                                                        |
| [**Dipinto**](inkoverlay-painted.md)                     | Si verifica quando l'oggetto **InkOverlay** ha completato il ridisegno.<br/>                                                                                                                                                                          |
| [**Disegno**](inkoverlay-painting.md)                   | Si verifica prima che l'oggetto **InkOverlay** venga ridisegnato.<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Si verifica quando la selezione dell'input penna all'interno del controllo viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                       |
| [**SelectionChanging**](inkoverlay-selectionchanging.md) | Si verifica quando la selezione dell'input penna all'interno del controllo sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)       | Si verifica quando la posizione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | Si verifica quando la posizione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | Si verifica quando la dimensione della selezione corrente viene modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                             |
| [**SelectionResizing**](inkoverlay-selectionresizing.md) | Si verifica quando la dimensione della selezione corrente sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                      |
| [**Stroke**](inkcollector-stroke.md)                     | Si verifica quando l'utente completa il disegno di un nuovo tratto su un tablet.<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | Si verifica dopo l'eliminazione dei tratti dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | Si verifica prima che i tratti vengano eliminati dalla proprietà [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                           |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Si verifica quando viene riconosciuto un movimento del sistema.<br/>                                                                                                                                                                                                    |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Si verifica quando un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene aggiunto al sistema.<br/>                                                                                                                                                                        |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Si verifica quando un [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene rimosso dal sistema.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Interfacce

La classe **InkOverlay** definisce queste interfacce.



| Interfaccia       | Descrizione                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | Questo oggetto implementa l'interfaccia com **IInkOverlay** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkOverlay** presenta questi metodi.



| Metodo                                                                              | Descrizione                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Disegna**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Imposta un rettangolo in cui ricreare l'input penna nell'oggetto **InkOverlay** .<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Restituisce lo stato corrente di un determinato evento dell'oggetto **InkOverlay** , ovvero se l'evento viene ascoltato o utilizzato.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Restituisce un valore che indica se l'oggetto **InkOverlay** è interessato a un movimento particolare.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera il rettangolo della finestra, in pixel, all'interno del quale viene disegnato l'input penna.<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Determina quale parte della selezione è stata raggiunta durante un hit test.<br/>                                                                             |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Questa modalità consente all'oggetto **InkOverlay** di raccogliere input penna da qualsiasi tablet collegato al Tablet PC.<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Imposta un valore che indica se è necessario ascoltare o utilizzare un evento specifico.<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Imposta l'interesse dell'oggetto **InkOverlay** in un movimento noto.<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Questa modalità consente all'oggetto **InkOverlay** di raccogliere l'input penna da un solo tablet. L'input penna da altre tavolette viene ignorato dall'oggetto **InkOverlay** .<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Imposta il rettangolo della finestra, in pixel, da utilizzare per eseguire il mapping dell'input penna alla finestra.<br/>                                                                    |



 

### <a name="properties"></a>Proprietà

La classe **InkOverlay** dispone di queste proprietà.



| Proprietà                                                                                       | Tipo di accesso           | Descrizione                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Lettura/Scrittura<br/> | Ottiene o imposta il valore che specifica se l'oggetto **InkOverlay** è associato dietro o davanti alla finestra nota.<br/>                                                       |
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica se l'oggetto **InkOverlay** ridisegna l'input penna quando la finestra viene invalidata.<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Sola lettura<br/>  | Ottiene un valore che specifica se l'input penna è attualmente in fase di disegno su un oggetto **InkOverlay** .<br/>                                                                                     |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Lettura/Scrittura<br/> | Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o entrambi sono riconosciuti durante la scrittura dell'utente.<br/>                                                                |
| [**Cursori**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Sola lettura<br/>  | Ottiene l'insieme di [**cursori**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) che è possibile utilizzare nell'area Inking.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto [**InkDrawingAttributes**](inkdrawingattributes-class.md) predefinito, che specifica gli attributi di disegno utilizzati durante il disegno e la visualizzazione dell'input penna.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta un interesse per gli aspetti del pacchetto associato all'input penna disegnato sull'oggetto **InkOverlay** .<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se viene eseguito il rendering dell'input penna quando viene disegnato.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se l'oggetto **InkOverlay** è in modalità input penna, modalità di eliminazione o modalità di selezione o modifica.<br/>                                                          |
| [**Abilitato**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica se l'oggetto **InkOverlay** raccoglie l'input penna.<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se l'input penna è stato cancellato dal tratto o dal punto.<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica la larghezza della descrizione della penna della gomma.<br/>                                                                                                              |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Lettura/Scrittura<br/> | Ottiene o imposta l'handle della finestra a cui è associato l'oggetto **InkOverlay** .<br/>                                                                                             |
| [**Input penna**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto [**InkDisp**](inkdisp-class.md) associato all'oggetto **InkOverlay** .<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Lettura/Scrittura<br/> | Ottiene o imposta i margini lungo l'asse x, in pixel.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Lettura/Scrittura<br/> | Ottiene o imposta i margini lungo l'asse y, in pixel.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Lettura/Scrittura<br/> | Ottiene o imposta l'icona del mouse personalizzata corrente.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte dell'oggetto.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto [**InkRenderer**](inkrenderer-class.md) utilizzato per creare input penna.<br/>                                                                                        |
| [**Selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Lettura/Scrittura<br/> | Ottiene o imposta la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) attualmente selezionata all'interno del controllo **InkOverlay** .<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica se viene eseguito il rendering dell'input penna come un solo colore quando il sistema è in modalità Contrasto elevato.<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un valore che specifica se l'interfaccia utente di selezione viene disegnata in un contrasto elevato quando il sistema è in modalità Contrasto elevato.<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Sola lettura<br/>  | Ottiene la tavoletta utilizzata attualmente dall'oggetto **InkOverlay** per raccogliere l'input.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Note sull'implementazione MFC

Se l'oggetto InkOverlay è stato collegato a un oggetto CView, rilasciare l'oggetto InkOverlay in risposta al \_ messaggio WM Destroy come illustrato nell'esempio seguente:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

L'oggetto **InkOverlay** è particolarmente adatto per l'acquisizione di note e per la creazione di un scarabocchio di base. L'utilizzo previsto principale di questo oggetto consiste nel visualizzare input penna come input penna.

In generale, l'interfaccia utente di run-time per questo oggetto è una finestra trasparente con input penna opaco.

Gli eventi [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)e [**MouseWheel**](inkcollector-mousewheel.md) restituiscono coordinate x e y in pixel e non le unità HIMETRIC associate allo spazio di input penna. Questo è dovuto al fatto che questi eventi sostituiscono gli eventi del mouse per le applicazioni non compatibili con la penna e queste applicazioni comprendono solo i pixel.

> [!Caution]  
> Se si imposta la proprietà [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) dell'oggetto **InkOverlay** su Infront, creare l'oggetto **InkOverlay** nel thread in cui è in esecuzione il form. L'applicazione potrebbe smettere di rispondere se l'oggetto **InkOverlay** viene creato in un thread diverso e la relativa proprietà **AttachMode** è impostata su Infront.

 

> [!Note]  
> Non è possibile rilasciare in modo sicuro l'oggetto **InkOverlay** in un thread non dell'interfaccia utente.

 

Per migliorare le prestazioni dell'applicazione, eliminare l'oggetto **InkOverlay** quando non è più necessario.

Se l'oggetto InkOverlay è stato collegato a un oggetto CView, rilasciare l'oggetto InkOverlay in risposta al \_ messaggio WM Destroy come illustrato nell'esempio seguente:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkCollector**](inkcollector-class.md)
</dt> <dt>

[Riferimento al controllo InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[Riferimento al controllo InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

