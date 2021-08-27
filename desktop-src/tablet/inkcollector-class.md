---
description: Rappresenta l'oggetto utilizzato per acquisire l'input penna dai dispositivi tablet disponibili.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: Classe InkCollector (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718177"
---
# <a name="inkcollector-class"></a>Classe InkCollector

Rappresenta l'oggetto utilizzato per acquisire l'input penna dai dispositivi tablet disponibili.

La creazione **del controllo InkCollector** dietro un controllo trasparente (ad esempio un controllo GroupBox con il set di proprietà **WS EX \_ \_ TRANSPARENT)** impedirà a **InkCollector** di raccogliere l'input penna.

**InkCollector** ha questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La **classe InkCollector** include questi eventi.



| Event                                                     | Descrizione                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Si verifica quando **InkCollector rileva** un pulsante del cursore verso il basso.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Si verifica quando **InkCollector rileva** un pulsante del cursore verso l'alto.<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | Si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.<br/>                                                                                                                                                                                 |
| [**Cursorinrange**](inkcollector-cursorinrange.md)       | Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto del tablet.<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Si verifica quando il cursore lascia l'intervallo di rilevamento fisico (prossimità) del contesto del tablet.<br/>                                                                                                                                                      |
| [**Doubleclick**](inkcollector-doubleclick.md)           | Si verifica quando si fa doppio clic sull'oggetto **InkCollector.**<br/>                                                                                                                                                                                         |
| [**Movimento**](inkcollector-gesture.md)                   | Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.<br/>                                                                                                                                                                                         |
| [**Mousedown**](inkcollector-mousedown.md)               | Si verifica quando il puntatore del mouse si trova **sull'oggetto InkCollector** e viene premuto un pulsante del mouse.<br/>                                                                                                                                                   |
| [**Mousemove**](inkcollector-mousemove.md)               | Si verifica quando il puntatore del mouse viene spostato **sull'oggetto InkCollector.**<br/>                                                                                                                                                                           |
| [**Mouseup**](inkcollector-mouseup.md)                   | Si verifica quando il puntatore del mouse viene posizionato **sull'oggetto InkCollector** e viene rilasciato un pulsante del mouse.<br/>                                                                                                                                                  |
| [**Mousewheel**](inkcollector-mousewheel.md)             | Si verifica quando la rotellina del mouse si sposta mentre **l'oggetto InkCollector** ha lo stato attivo.<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Si verifica quando viene visualizzato un pacchetto in air, che si verifica quando un utente sposta una penna vicino al tablet e il cursore si trova all'interno della finestra dell'oggetto **InkCollector** o l'utente sposta un mouse all'interno della finestra associata dell'oggetto **InkCollector.**<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Si verifica quando **l'oggetto InkCollector** riceve pacchetti.<br/>                                                                                                                                                                                          |
| [**infarto**](inkcollector-stroke.md)                     | Si verifica quando l'utente termina di disegnare un nuovo tratto su qualsiasi tablet.<br/>                                                                                                                                                                                  |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Si verifica quando viene riconosciuto un movimento di sistema.<br/>                                                                                                                                                                                                        |
| [**TabletAggiunta**](inkcollector-tabletadded.md)           | Si verifica quando [**un tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene aggiunto al sistema.<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Si verifica quando [**un Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) PC viene rimosso dal sistema.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Interfacce

La **classe InkCollector** definisce queste interfacce.



| Interfaccia         | Descrizione                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Questo oggetto implementa **l'interfaccia COM IInkCollector.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe InkCollector** include questi metodi.



| Metodo                                                                              | Descrizione                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Recupera lo stato corrente di un particolare **evento dell'oggetto InkCollector,** indipendentemente dal fatto che l'evento sia in ascolto o usato.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Recupera se **l'oggetto InkCollector** è interessato a un movimento specifico.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera il rettangolo della finestra, in pixel, all'interno del quale viene disegnato l'input penna.<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Questa modalità consente **all'oggetto InkCollector** di raccogliere input penna da qualsiasi tablet collegato al Tablet PC.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Modifica un valore che indica se un evento specifico deve essere in ascolto o usato.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Modifica l'interesse **dell'oggetto InkCollector** in un movimento noto.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Questa modalità consente **all'oggetto InkCollector** di raccogliere input penna da un solo tablet. L'input penna di altre compresse viene ignorato **dall'oggetto InkCollector.**<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Modifica il rettangolo della finestra, in pixel, da usare per eseguire il mapping dell'input penna disegnato alla finestra.<br/>                                                                    |



 

### <a name="properties"></a>Proprietà

La **classe InkCollector** ha queste proprietà.



| Proprietà                                                                             | Tipo di accesso          | Descrizione                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ridisegno automatico**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Sola lettura<br/> | Ottiene o imposta un valore che specifica se **InkCollector** ridisegna l'input penna quando la finestra viene invalidata.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Sola lettura<br/> | Ottiene un valore che specifica se l'input penna è attualmente disegnato su un **oggetto InkCollector.**<br/>                                                                                   |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Sola lettura<br/> | Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o entrambi vengono riconosciuti durante la scrittura da parte dell'utente.<br/>                                                                |
| [**Cursori**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Sola lettura<br/> | Ottiene la [**raccolta Cursors**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) disponibile per l'uso nell'area input penna.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Sola lettura<br/> | Ottiene o imposta [**l'oggetto InkDrawingAttributes**](inkdrawingattributes-class.md) predefinito, che specifica gli attributi di disegno utilizzati per disegnare e visualizzare l'input penna.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Sola lettura<br/> | Ottiene o imposta l'interesse per gli aspetti del pacchetto associato all'input penna disegnato **sull'oggetto InkCollector.**<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Sola lettura<br/> | Ottiene o imposta un valore che indica se viene eseguito il rendering dell'input penna mentre viene disegnato.<br/>                                                                                                       |
| [**Abilitato**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Sola lettura<br/> | Ottiene o imposta un valore che specifica se **l'oggetto InkCollector** raccoglie l'input penna.<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Sola lettura<br/> | Ottiene o imposta l'handle della finestra a cui è associato **l'oggetto InkCollector.**<br/>                                                                                           |
| [**Input penna**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Sola lettura<br/> | Ottiene o imposta [**l'oggetto InkDisp**](inkdisp-class.md) associato all'oggetto **InkCollector.**<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Sola lettura<br/> | Ottiene o imposta i margini lungo l'asse x, in pixel.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Sola lettura<br/> | Ottiene o imposta i margini lungo l'asse y, in pixel.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Sola lettura<br/> | Ottiene o imposta l'icona del mouse personalizzata corrente.<br/>                                                                                                                                       |
| [**Mousepointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Sola lettura<br/> | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte dell'oggetto .<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Sola lettura<br/> | Ottiene o imposta [**l'oggetto InkRenderer**](inkrenderer-class.md) utilizzato per disegnare l'input penna.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Sola lettura<br/> | Ottiene o imposta un valore che specifica se viene eseguito il rendering dell'input penna come un solo colore quando il sistema è in Contrasto elevato predefinita.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Sola lettura<br/> | Ottiene il dispositivo tablet attualmente **utilizzato dall'oggetto InkCollector** per raccogliere l'input.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

**L'oggetto InkCollector** raccoglie solo input penna e movimenti immessi nella finestra specifica a cui è associato. L'unico scopo di **InkCollector** è raccogliere l'input penna dall'hardware ,ad esempio tramite un oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkTablet,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) e consegnarlo a un'applicazione. Funge essenzialmente da origine che distribuisce l'input penna in uno o più [**oggetti InkDisp**](inkdisp-class.md) diversi, che fungono da contenitore che contengono l'input penna distribuito.

Per usare **un InkCollector,** crearlo, indicare in quale finestra raccogliere l'input penna disegnato e abilitarlo. Dopo essere stata abilitata, può essere impostata per raccogliere solo in una delle tre modalità (la modalità è specificata [**nell'enumerazione InkCollectionMode):**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)

-   InkOnly, in cui viene creato [**un oggetto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
-   GestureOnly, in cui viene creato [**un oggetto IInkGesture.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
-   InkAndGesture, in cui vengono creati un tratto, un movimento o potenzialmente entrambi, a seconda del modo in cui l'applicazione gestisce gli eventi.

Ciò significa che, per ogni spostamento di un cursore compreso nell'intervallo di un tablet, **InkCollector** raccoglie sempre un tratto o un movimento e talvolta entrambi. Il supporto dei movimenti è integrato con il riconoscimento dei movimenti Microsoft.

**InkCollector gestisce tutto** l'input del tablet. L'input penna può essere raccolto da tutte le compresse collegate (incluso il mouse) contemporaneamente. Le modifiche negli [**oggetti IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) possono causare la generazione di un evento da parte dell'oggetto **InkCollector.**

**InkCollector** gestisce anche l'elenco di cursori rilevati durante la sua esistenza. Quando **InkCollector** rileva un nuovo cursore, l'evento [**CursorInRange**](inkcollector-cursorinrange.md) viene generato con il *parametro newCursor* impostato su **VARIANT \_ TRUE.** Le applicazioni usano **InkCollector** per gestire i nuovi cursori.

È possibile **associare più inkCollector** a un handle di finestra specifico, anche se le aree di raccolta impostate nel costruttore o con il metodo [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) si sovrappongono. Tuttavia, l'unico modo in cui questo scenario funziona è se **ogni InkCollector** chiama [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) e usa un tablet univoco. Questo comportamento semplifica l'archiviazione dell'input penna in un oggetto separato per ogni tablet.

Si verifica un errore se il rettangolo di input della finestra di un **inkCollector abilitato** (impostato con la proprietà [**Enabled)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) si sovrappone al rettangolo di input della finestra di un altro **InkCollector abilitato.**

> [!Note]  
> La sovrapposizione può verificarsi senza errori, purché sia abilitato solo uno dei rettangoli di input in qualsiasi momento noto.

 

Gli [**eventi MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)e [**MouseWheel**](inkcollector-mousewheel.md) restituiscono le coordinate x e y in pixel e non le unità HIMETRIC associate allo spazio input penna. Questo perché questi eventi sostituiscono gli eventi del mouse delle applicazioni che non lo sono e queste applicazioni comprendono solo i pixel.

> [!Note]  
> **L'oggetto InkCollector** non può essere rilasciato in modo sicuro in un thread non dell'interfaccia utente.

 

Per migliorare le prestazioni dell'applicazione, eliminare **l'oggetto InkCollector** quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento sul controllo InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Informazioni di riferimento sul controllo InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

