---
description: L'oggetto PenInputPanel consente di aggiungere facilmente input penna sul posto alle applicazioni.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Classe PenInputPanel (Msinkaut. h)
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
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319159"
---
# <a name="peninputpanel-class"></a>Classe PenInputPanel

\[Deprecato. **PenInputPanel** è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).\]

L'oggetto **PenInputPanel** consente di aggiungere facilmente input penna sul posto alle applicazioni.

L'oggetto **PenInputPanel** è disponibile come oggetto collegato che consente di aggiungere la funzionalità del pannello di input di Tablet PC ai controlli esistenti. L'interfaccia utente è in gran parte obbligatoria dalla lingua di input corrente. È possibile scegliere il metodo di input predefinito per l'oggetto **PenInputPanel** , ovvero la grafia o la tastiera. L'utente finale può passare da un metodo di input all'altra usando i pulsanti dell'interfaccia utente.

**PenInputPanel** presenta questi tipi di membri:

-   [Enumerazioni](#enumerations)
-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="enumerations"></a>Enumerazioni

La classe **PenInputPanel** presenta queste enumerazioni.



| Enumerazione                    | Descrizione                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Definisce il tipo di input attualmente disponibile nell'oggetto **PenInputPanel** .<br/> |



 

### <a name="events"></a>Eventi

La classe **PenInputPanel** presenta questi eventi.



| Event                                                  | Descrizione                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Si verifica quando lo stato attivo per l'input cambia prima che l'oggetto **PenInputPanel** fosse in grado di inserire l'input dell'utente nel controllo associato.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Si verifica in seguito alla modifica dell'oggetto **PenInputPanel** tra layout.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Si verifica quando l'oggetto **PenInputPanel** viene spostato.<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Si verifica quando l'oggetto **PenInputPanel** è stato visualizzato o nascosto.<br/>                                                         |



 

### <a name="interfaces"></a>Interfacce

La classe **PenInputPanel** definisce queste interfacce.



| Interfaccia          | Descrizione                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Questo oggetto implementa l'interfaccia com **IPenInputPanel** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **PenInputPanel** presenta questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Invia l'input penna raccolto al riconoscimento e invia il risultato del riconoscimento.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Quando viene passato **true**, l'oggetto **PenInputPanel** tenta di inviare il testo al controllo collegato tramite il Framework di servizi di testo (TSF) e consente l'uso dell'interfaccia utente di correzione.<br/>    |
| [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Imposta la posizione dell'oggetto **PenInputPanel** su una posizione dello schermo statica.<br/>                                                                                                               |
| [**Aggiorna**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Aggiorna e ripristina le proprietà **PenInputPanel** basate sulle impostazioni del pannello di input di Tablet PC, posiziona automaticamente il pannello input penna e imposta l'interfaccia utente sul pannello predefinito.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **PenInputPanel** dispone di queste proprietà.



| Proprietà                                                                  | Tipo di accesso           | Descrizione                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'handle della finestra del controllo a cui è associato l'oggetto **PenInputPanel** .<br/>                                                                     |
| [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che specifica se l'oggetto **PenInputPanel** viene visualizzato quando lo stato attivo viene impostato utilizzando la penna.<br/>                                           |
| [**Occupato**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Sola lettura<br/>  | Ottiene un valore booleano che specifica se l'oggetto **PenInputPanel** sta attualmente elaborando l'input penna.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il tipo di pannello attualmente utilizzato per l'input all'interno dell'oggetto **PenInputPanel** .<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il tipo di pannello predefinito utilizzato per l'input all'interno dell'oggetto **PenInputPanel** .<br/>                                                         |
| [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta il nome di stringa del controllo del controllo utilizzato per il riconoscimento.<br/>                                                                                                    |
| [**Altezza**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Sola lettura<br/>  | Ottiene l'altezza dell'oggetto **PenInputPanel** nelle coordinate del client.<br/>                                                                                              |
| [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta l'offset tra il bordo sinistro dell'oggetto **PenInputPanel** e il bordo sinistro del controllo a cui è collegato.<br/>                             |
| [**Sinistra**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Sola lettura<br/>  | Ottiene la posizione orizzontale, o asse x, del bordo sinistro dell'oggetto **PenInputPanel** , in coordinate dello schermo.<br/>                                                   |
| [**In alto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Sola lettura<br/>  | Ottiene l'asse verticale, o asse y, della posizione del bordo superiore dell'oggetto **PenInputPanel** , in coordinate dello schermo.<br/>                                                      |
| [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta l'offset tra il bordo orizzontale più vicino dell'oggetto **PenInputPanel** e il bordo orizzontale più vicino al controllo a cui è collegato.<br/> |
| [**Visible**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore che indica se l'oggetto **PenInputPanel** è visibile.<br/>                                                                                |
| [**Larghezza**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Sola lettura<br/>  | Ottiene la larghezza dell'oggetto **PenInputPanel** nelle coordinate del client.<br/>                                                                                               |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Programmazione del pannello di input usando la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
