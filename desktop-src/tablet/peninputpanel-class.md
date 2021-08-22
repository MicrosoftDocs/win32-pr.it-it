---
description: L'oggetto PenInputPanel consente di aggiungere facilmente l'input penna sul posto alle applicazioni.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Classe PenInputPanel (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 58d27b97bb6683f32c145b92c1fda65fe0a786d5cb502e644580b57366119840
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708341"
---
# <a name="peninputpanel-class"></a>Classe PenInputPanel

\[Deprecato. **PenInputPanel** è stato sostituito dal [pannello di input di testo (TIP).](text-input-panel-reference.md)\]

**L'oggetto PenInputPanel** consente di aggiungere facilmente l'input penna sul posto alle applicazioni.

**L'oggetto PenInputPanel** è disponibile come oggetto associabile che consente di aggiungere funzionalità del Pannello input penna di Tablet PC ai controlli esistenti. L'interfaccia utente è ampiamente richiesta dalla lingua di input corrente. È possibile scegliere il metodo di input predefinito per **l'oggetto PenInputPanel,** la grafia o la tastiera. L'utente finale può passare da un metodo di input all'altro usando i pulsanti nell'interfaccia utente.

**PenInputPanel** ha questi tipi di membri:

-   [Enumerazioni](#enumerations)
-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="enumerations"></a>Enumerazioni

La **classe PenInputPanel** include queste enumerazioni.



| Enumerazione                    | Descrizione                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Definisce il tipo di input attualmente disponibile **nell'oggetto PenInputPanel.**<br/> |



 

### <a name="events"></a>Eventi

La **classe PenInputPanel** include questi eventi.



| Event                                                  | Descrizione                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Si verifica quando lo stato attivo dell'input cambia prima che l'oggetto **PenInputPanel** sia in grado di inserire l'input dell'utente nel controllo associato.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Si verifica quando **l'oggetto PenInputPanel** cambia tra i layout.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Si verifica quando **l'oggetto PenInputPanel** è in movimento.<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Si verifica quando **l'oggetto PenInputPanel** viene visualizzato o nascosto.<br/>                                                         |



 

### <a name="interfaces"></a>Interfacce

La **classe PenInputPanel** definisce queste interfacce.



| Interfaccia          | Descrizione                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Questo oggetto implementa **l'interfaccia COM IPenInputPanel.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe PenInputPanel** include questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Invia l'input penna raccolto al sistema di riconoscimento e invia il risultato del riconoscimento.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Quando viene passato **TRUE,** **PenInputPanel** tenta di inviare testo al controllo associato tramite Framework servizi di testo (TSF) e abilita l'uso dell'interfaccia utente di correzione.<br/>    |
| [**Moveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Imposta la posizione **dell'oggetto PenInputPanel** su una posizione statica dello schermo.<br/>                                                                                                               |
| [**Aggiorna**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Aggiorna e ripristina le proprietà **PenInputPanel** in base alle impostazioni del Pannello input penna di Tablet PC, posiziona automaticamente il pannello di input penna e imposta l'interfaccia utente sul pannello predefinito.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe PenInputPanel** ha queste proprietà.



| Proprietà                                                                  | Tipo di accesso           | Descrizione                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'handle di finestra del controllo a cui è associato l'oggetto **PenInputPanel.**<br/>                                                                     |
| [**Autoshow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che specifica se **l'oggetto PenInputPanel** viene visualizzato quando lo stato attivo viene impostato usando la penna.<br/>                                           |
| [**Occupato**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Sola lettura<br/>  | Ottiene un valore booleano che specifica se **l'oggetto PenInputPanel** sta attualmente elaborando l'input penna.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il tipo di pannello attualmente usato per l'input all'interno **dell'oggetto PenInputPanel.**<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il tipo di pannello predefinito utilizzato per l'input all'interno **dell'oggetto PenInputPanel.**<br/>                                                         |
| [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta il nome stringa del factoid utilizzato per il riconoscimento.<br/>                                                                                                    |
| [**Altezza**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Sola lettura<br/>  | Ottiene l'altezza **dell'oggetto PenInputPanel** nelle coordinate client.<br/>                                                                                              |
| [**Horizontaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'offset tra il bordo sinistro dell'oggetto **PenInputPanel** e il bordo sinistro del controllo a cui è associato.<br/>                             |
| [**Sinistra**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Sola lettura<br/>  | Ottiene la posizione orizzontale, o asse x, del bordo sinistro dell'oggetto **PenInputPanel,** nelle coordinate dello schermo.<br/>                                                   |
| [**In alto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Sola lettura<br/>  | Ottiene la posizione verticale, o asse y, del bordo superiore dell'oggetto **PenInputPanel,** in coordinate dello schermo.<br/>                                                      |
| [**Verticaloffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta l'offset tra il bordo orizzontale più vicino dell'oggetto **PenInputPanel** e il bordo orizzontale più vicino del controllo a cui è associato.<br/> |
| [**Visible**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se **l'oggetto PenInputPanel** è visibile.<br/>                                                                                |
| [**Larghezza**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Sola lettura<br/>  | Ottiene la larghezza **dell'oggetto PenInputPanel** nelle coordinate client.<br/>                                                                                               |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Programmazione del pannello di input tramite la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
