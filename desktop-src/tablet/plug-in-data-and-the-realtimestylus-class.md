---
description: I plug-in per la classe RealTimeStylus devono implementare l'interfaccia IStylusSyncPlugin o IStylusAsyncPlugin o entrambi.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Dati plug-in e classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0540d90f291acfef27a09df08ffff645c280d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480967"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Dati plug-in e classe RealTimeStylus

I plug-in per la [**classe RealTimeStylus**](realtimestylus-class.md) devono implementare l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) o entrambi. Anche se è necessario implementare tutti i metodi dell'interfaccia plug-in, il plug-in riceve solo chiamate ai metodi contrassegnati nella proprietà [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms574886(v=vs.100)) dei plug-in.

I metodi definiti nelle interfacce usano oggetti nello spazio dei nomi [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) per passare i dati della penna ai plug-in. La tabella seguente descrive gli oggetti dati che sono parametri nei metodi di notifica ed elenca il [valore DataInterestMask](/previous-versions/ms824787(v=msdn.10)) associato alla notifica.



| Dati plug-in                                                                                          | Valore DataInterestMask     | Descrizione                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Dati dell'applicazione personalizzati aggiunti da un plug-in.<br/>                                                                                                                                                                                                 |
| [Errordata](/previous-versions/ms824740(v=msdn.10))                                   | **Error (Errore) (Error (Errore)e)**                  | Informazioni sull'errore [**aggiunte dall'oggetto RealTimeStylus**](realtimestylus-class.md) in risposta a un'eccezione non gestita in uno dei plug-in.<br/>                                                                                          |
| [Inairpacketsdata](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Informazioni sui pacchetti per il movimento dello stilo mentre lo stilo è in aria sopra il digitalizzatore.<br/>                                                                                                                                                         |
| [Packetsdata](/previous-versions/ms824590(v=msdn.10))                               | **Pacchetti**                | Informazioni sui pacchetti per il movimento dello stilo mentre lo stilo tocca il digitalizzatore.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Informazioni aggiunte [**dall'oggetto RealTimeStylus**](realtimestylus-class.md) quando viene disabilitato.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Informazioni aggiunte [**dall'oggetto RealTimeStylus**](realtimestylus-class.md) quando viene abilitato.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Informazioni sul pulsante dello stilo specifico che viene premuto.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Informazioni sul pulsante dello stilo specifico che viene rilasciato.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **Stylusdown**             | Informazioni sul pacchetto per uno stilo quando lo stilo viene messo in contatto con il digitalizzatore.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Informazioni sullo stilo specifico che entra nell'area di input dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) o immette l'intervallo di rilevamento del digitalizzatore sopra l'area di input **dell'oggetto RealTimeStylus.**<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Informazioni sullo stilo specifico che lascia l'area di input dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) o lascia l'intervallo di rilevamento del digitalizzatore sopra l'area di input **dell'oggetto RealTimeStylus.**<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Informazioni sui pacchetti per uno stilo quando lo stilo viene rimosso dal digitalizzatore.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | Informazioni aggiunte [**dall'oggetto RealTimeStylus**](realtimestylus-class.md) quando rileva un movimento di sistema.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **TabletAggiunta**            | Informazioni [sull'oggetto Tablet](/previous-versions/ms827783(v=msdn.10)) da aggiungere.<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | Informazioni [sull'oggetto Tablet](/previous-versions/ms827783(v=msdn.10)) da rimuovere.<br/>                                                                                                                                              |



 

Per informazioni sul modo in cui [**l'oggetto RealTimeStylus**](realtimestylus-class.md) gestisce il flusso di dati della penna del tablet, vedere Utilizzo della [classe RealTimeStylus.](working-with-the-realtimestylus-class.md)

## <a name="data-interest"></a>Interesse per i dati

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) controlla la proprietà [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms574886(v=vs.100)) di un plug-in quando il plug-in viene aggiunto alla raccolta di plug-in sincrona o asincrona dell'oggetto **RealTimeStylus.** È quindi consigliabile usare la proprietà DataInterest per sottoscrivere tutte le notifiche usate da questa istanza del plug-in, tuttavia raramente, ma non a nessuna delle notifiche che questa istanza del plug-in non usa mai. Per le notifiche usate solo occasionalmente dal plug-in, controllare prima lo stato del plug-in nel metodo di notifica e restituire se la notifica non viene usata dal plug-in nello stato corrente.

Un plug-in riceve solo chiamate ai metodi contrassegnati nella proprietà [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms574886(v=vs.100)) del plug-in. Per altre informazioni sui valori possibili della proprietà **DataInterest** di un plug-in, vedere [l'enumerazione DataInterestMask.](/previous-versions/ms824787(v=msdn.10))

## <a name="timing"></a>Intervallo

I dati vengono accodati nell'oggetto [**RealTimeStylus**](realtimestylus-class.md) prima di essere passati ai plug-in nella raccolta di plug-in asincrona. Nell'elenco seguente vengono descritte alcune situazioni di cui potrebbe essere necessario fare conto durante la progettazione di un plug-in asincrono.

-   Quando [**l'oggetto RealTimeStylus**](realtimestylus-class.md) è disabilitato, il plug-in asincrono può ricevere altre notifiche in coda prima che venga chiamato il relativo metodo [RealTimeStylusDisabled.](/previous-versions/ms824774(v=msdn.10)) In questo caso, le chiamate dal plug-in ad alcuni metodi e proprietà dell'oggetto **RealTimeStylus** generano un'eccezione. Le informazioni rilevanti per il plug-in devono essere memorizzate nella cache quando **l'oggetto RealTimeStylus** è abilitato.
-   Il metodo [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) può rimuovere informazioni dalla coda di output. Di conseguenza, i plug-in asincroni non possono basarsi sulla ricezione di tutte le notifiche pertinenti.
-   Quando viene rimosso un oggetto [Tablet](/previous-versions/ms827783(v=msdn.10)) disponibile per l'oggetto [**RealTimeStylus,**](realtimestylus-class.md) il plug-in asincrono può ricevere una notifica dello stilo in coda per il tablet prima che venga chiamato il relativo metodo [TabletRemoved.](/previous-versions/bb361092(v=vs.100)) In questo caso, la chiamata al metodo [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) dell'oggetto **RealTimeStylus** non funziona. Le informazioni rilevanti per il plug-in devono essere memorizzate nella cache quando l'oggetto **RealTimeStylus** è abilitato o quando viene aggiunto un nuovo tablet.

A seconda dell'applicazione, è possibile migliorare le prestazioni quando si disabilita un [**oggetto RealTimeStylus.**](realtimestylus-class.md) Quando la proprietà [Enabled](/previous-versions/ms824832(v=msdn.10)) dell'oggetto **RealTimeStylus** è impostata su **FALSE,** i dati nelle code di input e output vengono elaborati fino a quando le code non sono vuote. È possibile chiamare il metodo [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) dell'oggetto **RealTimeStylus** per cancellare le code prima di disabilitare **l'oggetto RealTimeStylus.**

## <a name="enabled-and-disabled-data"></a>Dati abilitati e disabilitati

Quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato, ogni plug-in riceve una chiamata al relativo metodo [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusEnabled.](/previous-versions/ms824775(v=msdn.10)) **L'oggetto RealTimeStylusEnabledData** passato nella notifica contiene una raccolta di identificatori di contesto per i tablet disponibili quando l'oggetto **RealTimeStylus** è abilitato.

> [!Note]  
> Poiché i dati del plug-in per la raccolta di plug-in asincroni dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) vengono accodati, i plug-in asincroni possono ricevere dati prima di ricevere una chiamata al relativo metodo [RealTimeStylusDisabled,](/previous-versions/ms824774(v=msdn.10)) ma dopo la disabilitazione **dell'oggetto RealTimeStylus.** Si noti che alcuni metodi e proprietà **dell'oggetto RealTimeStylus** generano un'eccezione se l'oggetto **RealTimeStylus** è disabilitato.

 

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiama i metodi [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) sul thread da cui è abilitato l'oggetto **RealTimeStylus** o da cui viene aggiunto il plug-in sincrono.

In genere, aggiungere o rimuovere plug-in mentre [**l'oggetto RealTimeStylus**](realtimestylus-class.md) è disabilitato. Per altre informazioni sull'aggiunta e la rimozione di plug-in all'oggetto **RealTimeStylus,** vedere [Plug-in e classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Dati tablet

Quando un tablet che può essere utilizzato dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) viene aggiunto o rimosso dal Tablet PC mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** notifica ai plug-in che è stato aggiunto o rimosso un oggetto [Tablet.](/previous-versions/ms827783(v=msdn.10)) Ogni **oggetto RealTimeStylus** gestisce un elenco di identificatori univoci per gli oggetti Tablet con cui può interagire. **L'oggetto RealTimeStylus** include due metodi per la conversione tra l'identificatore univoco e l'oggetto Tablet, i metodi [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) e [GetTabletFromTabletContextId.](/previous-versions/ms825929(v=msdn.10))

> [!Note]  
> Le informazioni su un tablet non sono più disponibili [**dall'oggetto RealTimeStylus**](realtimestylus-class.md) dopo la rimozione del tablet dal Tablet PC.

 

## <a name="tablet-pen-data"></a>Dati della penna del Tablet PC

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) passa le informazioni sulla penna del tablet ai relativi plug-in in diversi metodi di notifica. Le informazioni sulla penna del tablet sono rappresentate da un [oggetto Stilo.](/previous-versions/ms824824(v=msdn.10)) Questo oggetto è uno snapshot dello stato della penna del tablet al momento della raccolta dei dati. Poiché i plug-in ricevono i dati della penna del tablet come parte del flusso di dati della penna del tablet, i plug-in devono usare le informazioni nell'oggetto Stilo invece di controllare lo stato corrente di una particolare penna del tablet tramite la [classe Cursor.](/previous-versions/ms839521(v=msdn.10))

Ogni [oggetto Stilo](/previous-versions/ms824824(v=msdn.10)) contiene l'identificatore di contesto del tablet per la tablet che ha generato i dati.

## <a name="system-gesture-data"></a>Dati movimenti di sistema

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) riceve i dati sui movimenti di sistema quando vengono riconosciuti dal Tablet PC. La tabella seguente descrive l'ordine in cui gli oggetti [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) si verificano nel flusso di dati della penna del tablet in relazione ad altri dati della penna del tablet.




| <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a> | Oggetti che precedono <a href="/previous-versions/ms824019(v=msdn.10)">l'oggetto SystemGestureData</a> | Oggetti che vengono dopo <a href="/previous-versions/ms824019(v=msdn.10)">l'oggetto SystemGestureData</a> | 
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <strong>Tocco</strong> | Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Oggetto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>DoubleTap</strong> | <a href="/previous-versions/ms824107(v=msdn.10)">L'oggetto StylusDownData,</a> <a href="/previous-versions/ms824019(v=msdn.10)">l'oggetto SystemGestureData</a> per il <strong>movimento di</strong> sistema Tap e gli [oggetti StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | Secondo oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | 
| <strong>RightTap</strong> | Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> e <a href="/previous-versions/ms824019(v=msdn.10)">oggetto SystemGestureData</a> per il membro <strong>HoldEnter</strong> dell'enumerazione <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure.</a><br /> | Oggetto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>Trascinamento</strong> | Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Oggetto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>RightDrag</strong> | Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Oggetto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>HoldEnter</strong> | Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Oggetto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /><blockquote>[!Note]<br />Questo movimento di sistema non viene riconosciuto se l'utente inizia un movimento <strong>di</strong> sistema <strong>Drag o RightDrag.</strong></blockquote><br /> | 
| <strong>HoldLeave</strong> | Non implementato.<br /> | Non implementato.<br /> | 
| <strong>HoverEnter</strong> | Diversi <a href="/previous-versions/ms824592(v=msdn.10)">oggetti InAirPacketsData</a> di bassa velocità media.<br /> | <blockquote>[!Note]<br />Potrebbe verificarsi un ritardo notevole prima di ricevere il <strong>movimento di sistema HoverEnter.</strong> <a href="realtimestylus-class.md"><strong>L'oggetto RealTimeStylus</strong></a> riceve questi dati solo se l'oggetto <strong>RealTimeStylus</strong> è collegato alla finestra o al controllo che si trova direttamente sotto la penna al momento del movimento del sistema.</blockquote><br /> | 
| <strong>HoverLeave</strong> | Oggetto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData per</a> il movimento di sistema <strong>HoverEnter</strong> e diversi <a href="/previous-versions/ms824592(v=msdn.10)">oggetti InAirPacketsData</a> di velocità media sufficiente.<br /> | <blockquote>[!Note]<br />Potrebbe verificarsi un notevole ritardo prima di ricevere il movimento di sistema <strong>HoverLeave.</strong> <a href="realtimestylus-class.md"><strong>L'oggetto RealTimeStylus</strong></a> riceve questi dati solo se l'oggetto <strong>RealTimeStylus</strong> è collegato alla finestra o al controllo che si trova direttamente sotto la penna al momento del movimento del sistema.</blockquote><br /> | 




 

## <a name="custom-stylus-data"></a>Dati dello stilo personalizzati

I dati dello stilo personalizzati possono essere aggiunti all'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiamando il [metodo AddCustomStylusDataToQueue.](/previous-versions/ms825761(v=msdn.10)) I dati dello stilo personalizzati possono essere aggiunti alle code dell'oggetto **RealTimeStylus** in una delle tre posizioni seguenti.

-   Quando il parametro *queue* è impostato su **Output**, i dati personalizzati vengono aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) dopo i dati attualmente elaborati dalla raccolta di plug-in sincroni.
-   Quando il parametro *queue* è impostato su **OutputImmediate,** i dati personalizzati vengono aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) prima dei dati attualmente elaborati dalla raccolta di plug-in sincrona.
-   Quando il parametro *queue* è impostato su **Input,** i dati personalizzati vengono aggiunti alla coda di input dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e inviati alla raccolta di plug-in sincrona prima dei nuovi dati dal flusso di dati della penna del tablet.

In ognuno dei casi precedenti, i dati aggiunti dai plug-in successivi nella raccolta di plug-in sincroni vengono aggiunti dopo i dati aggiunti dai plug-in precedenti.

> [!Note]  
> Se la chiamata al metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) viene effettuata da un plug-in sincrono in risposta a una chiamata a uno dei relativi metodi [**IStylusSyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) i dati dello stilo personalizzato vengono aggiunti al flusso di dati della penna del tablet in modo prevedibile; In caso contrario, viene aggiunto alla coda in relazione ai dati penna correnti che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) sta elaborando e non in relazione ai dati che il plug-in asincrono sta elaborando. Il metodo AddCustomStylusDataToQueue genera un'eccezione se **l'oggetto RealTimeStylus** è disabilitato.

 

I dati dello stilo personalizzati vengono aggiunti alla coda come oggetto [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) e i plug-in ricevono questi dati tramite il metodo [Microsoft.StylusInput.IStylusSyncPlugin.CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) [o Microsoft.StylusInput.IStylusAsyncPlugin.CustomStylusDataAdded.](/previous-versions/ms824770(v=msdn.10))

Gli [**oggetti DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e [**GestureRecognizer**](gesturerecognizer-class.md) possono aggiungere dati dello stilo personalizzati alla coda. Per altre informazioni sugli **oggetti DynamicRenderer** e **GestureRecognizer,** vedere [Plug-in dynamic-renderer](dynamic-renderer-plug-ins.md) e [plug-in di](recognizer-plug-ins.md)riconoscimento.

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiama il metodo [Microsoft.StylusInput.IStylusSyncPlugin.CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) sul thread da cui riceve la chiamata al relativo metodo [AddCustomStylusDataToQueue.](/previous-versions/ms825761(v=msdn.10))

Il diagramma seguente illustra l'aggiunta di dati dello stilo personalizzati alla coda di output con il *parametro queue* impostato su **Output**.

![illustrazione che mostra il flusso di dati dello stilo personalizzato alla coda di output ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

In questo diagramma i cerchi con lettere "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. La lettera circolare "C" rappresenta i dati della penna del tablet che **l'oggetto RealTimeStylus** sta elaborando. Viene inviato alla raccolta di plug-in sincroni e inserito nella coda di output. I cerchi numerati "1", "2" e "3" rappresentano i dati dello stilo personalizzati aggiunti alla coda di output rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono in risposta ai dati della penna del tablet rappresentati da "C". I plug-in hanno aggiunto i dati dello stilo personalizzati con il parametro *queue* impostato su **StylusQueues.** Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i futuri dati della penna del tablet.

Il diagramma seguente illustra l'aggiunta di dati dello stilo personalizzati alla coda di output con il *parametro queue* impostato su **OutputImmediate.**

![Diagramma che mostra il flusso di dati dello stilo personalizzato alla coda di output.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

In questo diagramma i cerchi con lettere "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. La lettera circolare "C" rappresenta i dati della penna del tablet che **l'oggetto RealTimeStylus** sta elaborando. Viene inviato alla raccolta di plug-in sincroni e inserito nella coda di output. I cerchi numerati "1", "2" e "3" rappresentano i dati dello stilo personalizzati aggiunti alla coda di output rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono in risposta ai dati della penna del tablet rappresentati da "C". I plug-in hanno aggiunto i dati dello stilo personalizzato con il parametro *queue* impostato su **OutputImmediate.** Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i futuri dati della penna del tablet.

Il diagramma seguente illustra l'aggiunta di dati dello stilo personalizzati alla coda di input.

![illustrazione che mostra il flusso di dati dello stilo personalizzato alla coda di output](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

In questo diagramma i cerchi con lettere "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. La lettera circolare "C" rappresenta i dati della penna del tablet che **l'oggetto RealTimeStylus** sta elaborando. Viene inviato alla raccolta di plug-in sincroni e inserito nella coda di output. I cerchi numerati "1", "2" e "3" rappresentano i dati dello stilo personalizzati aggiunti alla coda di input rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono in risposta ai dati della penna del tablet rappresentati da "C". I plug-in hanno aggiunto i dati dello stilo personalizzato con il parametro *queue* impostato su **Input.** I dati dello stilo personalizzati numerati "1" vengono quindi passati ai plug-in sincroni e quindi alla coda di output prima dei dati dello stilo personalizzati numerati "2" e "3", entrambi elaborati prima dell'elaborazione dei dati della penna del tablet successivi. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i futuri dati della penna del tablet.

## <a name="error-data"></a>Dati errore

Quando un plug-in genera un'eccezione, il normale flusso di dati viene interrotto. [**L'oggetto RealTimeStylus**](realtimestylus-class.md) genera un [oggetto ErrorData](/previous-versions/ms824740(v=msdn.10)) e chiama:

-   Metodo [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) del plug-in che ha generato l'eccezione.
-   Metodo [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) dei plug-in rimanenti nella raccolta.

Se il plug-in che ha generato l'eccezione è un plug-in sincrono, l'oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) viene aggiunto alla coda di output. [**L'oggetto RealTimeStylus**](realtimestylus-class.md) riprende quindi la normale elaborazione dei dati originali.

Il diagramma seguente illustra l'aggiunta di dati di errore ai dati della penna del tablet.

![flusso di dati dello stilo personalizzato alla coda di output con l'aggiunta di dati di errore](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

In questo diagramma i cerchi con lettere "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. La lettera circolare "C" rappresenta i dati della penna del tablet che **l'oggetto RealTimeStylus** sta elaborando. Il cerchio con lettera "e" rappresenta un oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) generato dall'oggetto **RealTimeStylus** quando il secondo plug-in sincrono, plug-in sincrono 2, genera un'eccezione durante l'elaborazione di "C". **L'oggetto RealTimeStylus** sospende quindi l'elaborazione di "C" e passa "e" al plug-in che ha generato l'eccezione e a tutti i plug-in successivi. L'oggetto **RealTimeStylus** inserisce quindi "e" nella coda di output e riprende l'elaborazione di "C", che viene passata ai plug-in rimanenti nella raccolta di plug-in sincroni e inserita nella coda di output dopo "e". Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i futuri dati della penna del tablet.

Se un plug-in genera un'eccezione dal relativo metodo Error, l'oggetto [**RealTimeStylus**](realtimestylus-class.md) rileva l'eccezione ma non genera un nuovo [oggetto ErrorData.](/previous-versions/ms824740(v=msdn.10)) Ciò consente di evitare la ricorsione.

I dati dell'errore vengono aggiunti alla coda di output dopo tutti i dati dello stilo personalizzati aggiunti nella posizione **OutputImmediate** prima dell'eccezione che ha creato i dati di errore e prima di tutti i dati dello stilo personalizzati aggiunti nella posizione **OutputImmediate** dai plug-in successivi nella raccolta di plug-in sincroni.

Il diagramma seguente illustra come i dati degli errori vengono aggiunti alla coda di output in relazione ai dati personalizzati aggiunti alla **coda OutputImmediate.**

![dati di errore aggiunti alla coda di output in relazione ai dati personalizzati aggiunti alla coda outputimmediate.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

In questo diagramma i cerchi con lettere "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. La lettera circolare "C" rappresenta i dati della penna del tablet che **l'oggetto RealTimeStylus** sta elaborando. I cerchi numerati "1", "2" e "3" vengono aggiunti rispettivamente dal primo, secondo e terzo plug-in sincrono alla coda **OutputImmediate** in risposta ai dati rappresentati dalla lettera "C" del cerchio. Il cerchio con lettera "e" rappresenta i dati di errore generati in risposta a un'eccezione generata dal secondo plug-in dopo che il secondo plug-in ha aggiunto dati personalizzati alla coda di output nella posizione **OutputImmediate.**

Se un plug-in sincrono aggiunge dati dello stilo personalizzati alla coda di input in risposta ai dati di errore, i dati vengono aggiunti immediatamente prima dei dati dell'errore. Se uno dei plug-in sincroni aggiunge dati dello stilo personalizzati alla coda di output in corrispondenza della posizione **Output** in risposta ai dati di errore, i dati vengono aggiunti immediatamente dopo i dati dell'errore.

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) chiama il metodo [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) sul thread da cui viene generata l'eccezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft.Ink.Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft.stylusinput.plugindata](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Uso della classe RealTimeStylus](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
