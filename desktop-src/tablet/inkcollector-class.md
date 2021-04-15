---
description: Rappresenta l'oggetto utilizzato per acquisire l'input penna da dispositivi tablet disponibili.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: Classe InkCollector (Msinkaut. h)
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
ms.openlocfilehash: 17eff388a759b9b0873929447e4c8fe008e2fba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525279"
---
# <a name="inkcollector-class"></a>Classe InkCollector

Rappresenta l'oggetto utilizzato per acquisire l'input penna da dispositivi tablet disponibili.

La creazione del controllo **InkCollector** dietro un controllo trasparente, ad esempio un GroupBox con il set di proprietà **WS \_ ex \_ trasparente** , impedisce a **InkCollector** di raccogliere input penna.

**InkCollector** presenta questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La classe **InkCollector** presenta questi eventi.



| Event                                                     | Descrizione                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | Si verifica quando l'oggetto **InkCollector** rileva un pulsante del cursore inattivo.<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | Si verifica quando l'oggetto **InkCollector** rileva un pulsante del cursore.<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.<br/>                                                                                                                                                                                 |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.<br/>                                                                                                                                                      |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Si verifica quando si fa doppio clic sull'oggetto **InkCollector** .<br/>                                                                                                                                                                                         |
| [**Movimento**](inkcollector-gesture.md)                   | Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.<br/>                                                                                                                                                                                         |
| [**MouseDown**](inkcollector-mousedown.md)               | Si verifica quando il puntatore del mouse si trova sull'oggetto **InkCollector** e viene premuto un pulsante del mouse.<br/>                                                                                                                                                   |
| [**MouseMove**](inkcollector-mousemove.md)               | Si verifica quando il puntatore del mouse viene spostato sull'oggetto **InkCollector** .<br/>                                                                                                                                                                           |
| [**MouseUp**](inkcollector-mouseup.md)                   | Si verifica quando il puntatore del mouse si trova sull'oggetto **InkCollector** e viene rilasciato un pulsante del mouse.<br/>                                                                                                                                                  |
| [**MouseWheel**](inkcollector-mousewheel.md)             | Si verifica quando viene spostata la rotellina del mouse mentre l'oggetto **InkCollector** dispone dello stato attivo.<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | Si verifica quando viene rilevato un pacchetto in aria, che si verifica quando un utente sposta una penna accanto alla tavoletta e il cursore si trova all'interno della finestra dell'oggetto **InkCollector** oppure l'utente sposta il mouse all'interno della finestra associata dell'oggetto **InkCollector** .<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | Si verifica quando l'oggetto **InkCollector** riceve i pacchetti.<br/>                                                                                                                                                                                          |
| [**Stroke**](inkcollector-stroke.md)                     | Si verifica quando l'utente completa il disegno di un nuovo tratto su un tablet.<br/>                                                                                                                                                                                  |
| [**SystemGesture**](inkcollector-systemgesture.md)       | Si verifica quando viene riconosciuto un movimento del sistema.<br/>                                                                                                                                                                                                        |
| [**TabletAdded**](inkcollector-tabletadded.md)           | Si verifica quando un [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene aggiunto al sistema.<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | Si verifica quando un [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene rimosso dal sistema.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Interfacce

La classe **InkCollector** definisce queste interfacce.



| Interfaccia         | Descrizione                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | Questo oggetto implementa l'interfaccia com **IInkCollector** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkCollector** presenta questi metodi.



| Metodo                                                                              | Descrizione                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Recupera lo stato corrente di un determinato evento dell'oggetto **InkCollector** , ovvero se l'evento viene ascoltato o utilizzato.<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Recupera un valore che indica se l'oggetto **InkCollector** è interessato a un movimento particolare.<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Recupera il rettangolo della finestra, in pixel, all'interno del quale viene disegnato l'input penna.<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Questa modalità consente all'oggetto **InkCollector** di raccogliere input penna da qualsiasi tablet collegato al Tablet PC.<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Modifica un valore che indica se è necessario ascoltare o utilizzare un evento specifico.<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Modifica l'interesse dell'oggetto **InkCollector** in un movimento noto.<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Questa modalità consente all'oggetto **InkCollector** di raccogliere l'input penna da un solo tablet. L'input penna da altre tavolette viene ignorato dall'oggetto **InkCollector** .<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Modifica il rettangolo della finestra, in pixel, da utilizzare per eseguire il mapping dell'input penna alla finestra.<br/>                                                                    |



 

### <a name="properties"></a>Proprietà

La classe **InkCollector** dispone di queste proprietà.



| Proprietà                                                                             | Tipo di accesso          | Descrizione                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Sola lettura<br/> | Ottiene o imposta un valore che specifica se l'oggetto **InkCollector** ridisegna l'input penna quando la finestra viene invalidata.<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Sola lettura<br/> | Ottiene un valore che specifica se l'input penna è attualmente in fase di disegno su un oggetto **InkCollector** .<br/>                                                                                   |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Sola lettura<br/> | Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o entrambi sono riconosciuti durante la scrittura dell'utente.<br/>                                                                |
| [**Cursori**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Sola lettura<br/> | Ottiene l'insieme di [**cursori**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) che è possibile utilizzare nell'area Inking.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Sola lettura<br/> | Ottiene o imposta l'oggetto [**InkDrawingAttributes**](inkdrawingattributes-class.md) predefinito, che specifica gli attributi di disegno utilizzati durante il disegno e la visualizzazione dell'input penna.<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Sola lettura<br/> | Ottiene o imposta un interesse per gli aspetti del pacchetto associato all'input penna disegnato sull'oggetto **InkCollector** .<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Sola lettura<br/> | Ottiene o imposta un valore che indica se viene eseguito il rendering dell'input penna quando viene disegnato.<br/>                                                                                                       |
| [**Abilitato**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Sola lettura<br/> | Ottiene o imposta un valore che specifica se l'oggetto **InkCollector** raccoglie l'input penna.<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Sola lettura<br/> | Ottiene o imposta l'handle della finestra a cui è associato l'oggetto **InkCollector** .<br/>                                                                                           |
| [**Input penna**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Sola lettura<br/> | Ottiene o imposta l'oggetto [**InkDisp**](inkdisp-class.md) associato all'oggetto **InkCollector** .<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Sola lettura<br/> | Ottiene o imposta i margini lungo l'asse x, in pixel.<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Sola lettura<br/> | Ottiene o imposta i margini lungo l'asse y, in pixel.<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Sola lettura<br/> | Ottiene o imposta l'icona del mouse personalizzata corrente.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Sola lettura<br/> | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte dell'oggetto.<br/>                                                |
| [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Sola lettura<br/> | Ottiene o imposta l'oggetto [**InkRenderer**](inkrenderer-class.md) utilizzato per creare input penna.<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Sola lettura<br/> | Ottiene o imposta un valore che specifica se viene eseguito il rendering dell'input penna come un solo colore quando il sistema è in modalità Contrasto elevato.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Sola lettura<br/> | Ottiene la tavoletta utilizzata attualmente dall'oggetto **InkCollector** per raccogliere l'input.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

L'oggetto **InkCollector** raccoglie solo input penna e movimenti che sono input nella finestra specifica a cui è associato. L'unico scopo di **InkCollector** è raccogliere input penna dall'hardware, ad esempio tramite un oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) , e distribuirlo a un'applicazione. Essenzialmente funge da origine che distribuisce l'input penna in uno o più oggetti [**InkDisp**](inkdisp-class.md) diversi, che fungono da contenitore che contengono l'input penna distribuito.

Per usare un oggetto **InkCollector**, è necessario crearlo, indicare in quale finestra raccogliere l'input penna e abilitarlo. Una volta abilitato, può essere impostato per la raccolta solo in una delle tre modalità (la modalità è specificata nell'enumerazione [**InkCollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) ):

-   InkOnly, in cui viene creato un oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .
-   GestureOnly, in cui viene creato un oggetto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .
-   InkAndGesture, in cui viene creato un tratto, un movimento o potenzialmente entrambi, a seconda del modo in cui l'applicazione gestisce gli eventi.

Ciò significa che, per ogni spostamento di un cursore compreso nell'intervallo di un tablet, l'oggetto **InkCollector** raccoglie sempre un tratto o un movimento e talvolta entrambi. Il supporto dei movimenti viene incorporato usando il riconoscitore di movimento Microsoft.

Un oggetto **InkCollector** gestisce tutto il tablet input. L'input penna può essere raccolto contemporaneamente da tutti i tablet collegati (incluso il mouse). Le modifiche apportate agli oggetti [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) e [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) possono causare l'attivazione di un evento da parte dell'oggetto **InkCollector** .

Un oggetto **InkCollector** gestisce anche l'elenco dei cursori incontrati durante la sua esistenza. Quando l'oggetto **InkCollector** rileva un nuovo cursore, l'evento [**CursorInRange**](inkcollector-cursorinrange.md) viene attivato con il parametro *NewCursor* impostato su **Variant \_ true**. Le applicazioni utilizzano l'oggetto **InkCollector** per gestire i nuovi cursori.

È possibile associare più di un oggetto **InkCollector** a un particolare handle di finestra, anche se le relative aree di raccolta, impostate nel costruttore o con il metodo [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) , si sovrappongono. Tuttavia, l'unico modo in cui funziona questo scenario è se ogni **InkCollector** chiama [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) e usa un tablet univoco. Questo comportamento consente di archiviare facilmente l'input penna in un oggetto separato per ogni tablet.

Si verifica un errore se il rettangolo di input della finestra di un oggetto **InkCollector** abilitato (impostato con la proprietà [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) ) si sovrappone al rettangolo di input della finestra di un altro oggetto **InkCollector** abilitato.

> [!Note]  
> La sovrapposizione può verificarsi senza un errore purché solo uno dei rettangoli di input sia abilitato in qualsiasi momento noto.

 

Gli eventi [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)e [**MouseWheel**](inkcollector-mousewheel.md) restituiscono le coordinate x e y in pixel e non le unità HIMETRIC associate allo spazio di input penna. Questo è dovuto al fatto che questi eventi sostituiscono gli eventi del mouse per le applicazioni non compatibili con la penna e queste applicazioni comprendono solo i pixel.

> [!Note]  
> Non è possibile rilasciare in modo sicuro l'oggetto **InkCollector** in un thread non dell'interfaccia utente.

 

Per migliorare le prestazioni dell'applicazione, eliminare l'oggetto **InkCollector** quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento al controllo InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Classe InkDisp**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay (classe)**](inkoverlay-class.md)
</dt> <dt>

[Riferimento al controllo InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

