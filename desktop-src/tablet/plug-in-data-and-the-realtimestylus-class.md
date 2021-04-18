---
description: I plug-in per la classe RealTimeStylus devono implementare l'interfaccia IStylusSyncPlugin o IStylusAsyncPlugin o entrambi.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Dati plug-in e classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372b3d297edbad6d339285f45e92118184fa2cfc
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104562611"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Dati plug-in e classe RealTimeStylus

I plug-in per la classe [**RealTimeStylus**](realtimestylus-class.md) devono implementare l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) o entrambi. Sebbene sia necessario implementare tutti i metodi di interfaccia plug-in, il plug-in riceve solo le chiamate ai metodi contrassegnati nella proprietà plug-in [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) .

I metodi definiti nelle interfacce utilizzano oggetti nello spazio dei nomi [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) per passare i dati della penna ai plug-in. Nella tabella seguente vengono descritti gli oggetti dati che sono parametri nei metodi di notifica e viene elencato il valore [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) associato alla notifica.



| Dati plug-in                                                                                          | Valore DataInterestMask     | Descrizione                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Dati dell'applicazione personalizzati aggiunti da un plug-in.<br/>                                                                                                                                                                                                 |
| [ErrorData](/previous-versions/ms824740(v=msdn.10))                                   | **Error (Errore) (Error (Errore)e)**                  | Informazioni sugli errori aggiunte dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) in risposta a un'eccezione non gestita in uno dei relativi plug-in.<br/>                                                                                          |
| [InAirPacketsData](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Informazioni sui pacchetti per lo stilo quando lo stilo è in aria sopra il digitalizzatore.<br/>                                                                                                                                                         |
| [PacketsData](/previous-versions/ms824590(v=msdn.10))                               | **Pacchetti**                | Informazioni sui pacchetti per il movimento dello stilo quando lo stilo tocca il digitalizzatore.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Informazioni aggiunte dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) quando questo viene disabilitato.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Informazioni aggiunte dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) quando viene abilitata.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Informazioni sul pulsante dello stilo premuto.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Informazioni sul particolare pulsante dello stilo rilasciato.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | Le informazioni sui pacchetti per uno stilo come lo stilo vengono portate in contatto con il digitalizzatore.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Informazioni sul particolare stilo che sta immettendo l'area di input dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) o immettendo l'intervallo di rilevamento del digitalizzatore sopra l'area di input dell'oggetto **RealTimeStylus** .<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Informazioni sul particolare stilo che lascia l'area di input dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) o che lascia l'intervallo di rilevamento del digitalizzatore sopra l'area di input dell'oggetto **RealTimeStylus** .<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Le informazioni sui pacchetti per uno stilo come lo stilo vengono sollevate dal digitalizzatore.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | Informazioni aggiunte dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) quando viene rilevato un movimento di sistema.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **TabletAdded**            | Informazioni sull'oggetto [Tablet](/previous-versions/ms827783(v=msdn.10)) da aggiungere.<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | Informazioni sull'oggetto [Tablet](/previous-versions/ms827783(v=msdn.10)) da rimuovere.<br/>                                                                                                                                              |



 

Per informazioni sul modo in cui l'oggetto [**RealTimeStylus**](realtimestylus-class.md) gestisce il flusso di dati della penna del tablet, vedere [utilizzo della classe RealTimeStylus](working-with-the-realtimestylus-class.md).

## <a name="data-interest"></a>Interesse per i dati

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) controlla la proprietà [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) di un plug-in quando il plug-in viene aggiunto alla raccolta di plug-in sincrona o asincrona dell'oggetto **RealTimeStylus** . Pertanto, è consigliabile utilizzare la proprietà DataInterest per sottoscrivere tutte le notifiche utilizzate da questa istanza del plug-in, tuttavia raramente, ma non a nessuna delle notifiche utilizzate da questa istanza del plug-in. Per le notifiche che il plug-in USA solo occasionalmente, controllare prima lo stato del plug-in nel metodo di notifica e restituire se la notifica non viene usata dal plug-in nello stato corrente.

Un plug-in riceve solo le chiamate ai metodi contrassegnati nella proprietà [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) di plug-in. Per ulteriori informazioni sui valori possibili della proprietà **DataInterest** di un plug-in, vedere l'enumerazione [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .

## <a name="timing"></a>Intervallo

I dati vengono accodati nell'oggetto [**RealTimeStylus**](realtimestylus-class.md) prima che vengano passati ai plug-in nella raccolta di plug-in asincroni. Nell'elenco seguente vengono descritte alcune situazioni che può essere necessario tenere in considerazione durante la progettazione di un plug-in asincrono.

-   Quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è disabilitato, il plug-in asincrono può ricevere altre notifiche in coda prima che venga chiamato il metodo [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) . In questa situazione, le chiamate dal plug-in ad alcuni metodi e proprietà dell'oggetto **RealTimeStylus** generano un'eccezione. Le informazioni relative al plug-in devono essere memorizzate nella cache quando l'oggetto **RealTimeStylus** è abilitato.
-   Il metodo [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) può rimuovere informazioni dalla coda di output. Pertanto, i plug-in asincroni non possono basarsi sulla ricezione di tutte le notifiche pertinenti.
-   Quando un oggetto [Tablet](/previous-versions/ms827783(v=msdn.10)) disponibile per l'oggetto [**RealTimeStylus**](realtimestylus-class.md) viene rimosso, il plug-in asincrono può ricevere una notifica dello stilo in coda per il tablet prima che venga chiamato il metodo [TabletRemoved](/previous-versions/bb361092(v=vs.100)) . In questa situazione, la chiamata al metodo [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) dell'oggetto **RealTimeStylus** non funziona. Le informazioni relative al plug-in devono essere memorizzate nella cache quando l'oggetto **RealTimeStylus** è abilitato o quando viene aggiunto un nuovo tablet.

A seconda dell'applicazione, è possibile migliorare le prestazioni quando si disabilita un oggetto [**RealTimeStylus**](realtimestylus-class.md) . Quando la proprietà [Enabled](/previous-versions/ms824832(v=msdn.10)) dell'oggetto **RealTimeStylus** è impostata su **false**, i dati nelle code di input e di output vengono elaborati fino a quando le code non sono vuote. È possibile chiamare il metodo [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) dell'oggetto **RealTimeStylus** per cancellare le code prima di disabilitare l'oggetto **RealTimeStylus** .

## <a name="enabled-and-disabled-data"></a>Dati abilitati e disabilitati

Quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato, ogni plug-in riceve una chiamata al relativo metodo [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) . L'oggetto **RealTimeStylusEnabledData** passato nella notifica contiene una raccolta di identificatori di contesto per le tavolette disponibili nel momento in cui l'oggetto **RealTimeStylus** è abilitato.

> [!Note]  
> Poiché i dati del plug-in per la raccolta di plug-in asincrona dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) sono accodati, i plug-in asincroni possono ricevere dati prima di ricevere una chiamata al metodo [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , ma dopo che l'oggetto **RealTimeStylus** è stato disabilitato. Si noti che alcuni metodi e proprietà dell'oggetto **RealTimeStylus** generano un'eccezione se l'oggetto **RealTimeStylus** è disabilitato.

 

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiama i metodi [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) e [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) sul thread da cui è abilitato l'oggetto **RealTimeStylus** o da cui viene aggiunto il plug-in sincrono.

In genere, aggiungere o rimuovere plug-in mentre l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è disabilitato. Per ulteriori informazioni sull'aggiunta e la rimozione di plug-in nell'oggetto **RealTimeStylus** , vedere [plug-in e la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Dati Tablet

Quando un tablet che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) può utilizzare viene aggiunto o rimosso dal Tablet PC mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** notifica ai plug-in che un oggetto [Tablet](/previous-versions/ms827783(v=msdn.10)) è stato aggiunto o rimosso. Ogni oggetto **RealTimeStylus** gestisce un elenco di identificatori univoci per gli oggetti Tablet con cui può interagire. L'oggetto **RealTimeStylus** dispone di due metodi per la conversione tra l'identificatore univoco e l'oggetto Tablet, i metodi [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) e [GetTabletFromTabletContextId](/previous-versions/ms825929(v=msdn.10)) .

> [!Note]  
> Le informazioni su un tablet non sono più disponibili dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) dopo che il tablet è stato rimosso dal Tablet PC.

 

## <a name="tablet-pen-data"></a>Dati della penna del Tablet

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) passa informazioni sulla penna del Tablet ai relativi plug-in in una serie di metodi di notifica. Le informazioni sulla penna del tablet sono rappresentate da un oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) . Questo oggetto è uno snapshot dello stato della penna da tavoletta al momento della raccolta dei dati. Poiché i plug-in ricevono i dati della penna del tablet come parte del flusso di dati della penna del tablet, i plug-in devono usare le informazioni nell'oggetto stilo anziché controllare lo stato corrente di una particolare penna del tablet tramite la classe [Cursor](/previous-versions/ms839521(v=msdn.10)) .

Ogni oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) contiene l'identificatore di contesto del tablet per il tablet che ha generato i dati.

## <a name="system-gesture-data"></a>Dati del movimento di sistema

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) riceve i dati sui movimenti del sistema come vengono riconosciuti dal Tablet PC. Nella tabella seguente viene descritto l'ordine in cui si verificano gli oggetti [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) nel flusso di dati della penna del tablet in relazione ad altri dati della penna del Tablet PC.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a></th>
<th>Oggetti che precedono l'oggetto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a></th>
<th>Oggetti che derivano dall'oggetto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tocco</strong></td>
<td>Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>Oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>DoubleTap</strong></td>
<td>Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> , l'oggetto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> per il gesto del sistema <strong>Tap</strong> e gli oggetti [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
<td>Secondo oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>RightTap</strong></td>
<td>Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> e oggetto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> per il membro <strong>HoldEnter</strong> dell'enumerazione <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure</a> .<br/></td>
<td>Oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>Trascinamento</strong></td>
<td>Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>Oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="odd">
<td><strong>RightDrag se</strong></td>
<td>Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>Oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>HoldEnter</strong></td>
<td>Oggetto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>Oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/>
<blockquote>
[!Note]<br />
Questo movimento di sistema non viene riconosciuto se l'utente inizia un movimento di sistema di <strong>trascinamento</strong> o <strong>RightDrag se</strong> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoldLeave</strong></td>
<td>Non implementato.<br/></td>
<td>Non implementato.<br/></td>
</tr>
<tr class="even">
<td><strong>HoverEnter</strong></td>
<td>Diversi oggetti <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> di velocità media bassa.<br/></td>
<td><blockquote>
[!Note]<br />
È possibile che si verifichi un ritardo evidente prima della ricezione del movimento del sistema <strong>HoverEnter</strong> . L'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> riceve questi dati solo se l'oggetto <strong>RealTimeStylus</strong> è associato alla finestra o al controllo che si trova direttamente sotto la penna al momento del movimento del sistema.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoverLeave</strong></td>
<td>Oggetto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> per il gesto del sistema <strong>HoverEnter</strong> e diversi oggetti <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> di velocità media sufficiente.<br/></td>
<td><blockquote>
[!Note]<br />
È possibile che si verifichi un ritardo evidente prima della ricezione del movimento del sistema <strong>HoverLeave</strong> . L'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> riceve questi dati solo se l'oggetto <strong>RealTimeStylus</strong> è associato alla finestra o al controllo che si trova direttamente sotto la penna al momento del movimento del sistema.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="custom-stylus-data"></a>Dati stilo personalizzati

È possibile aggiungere dati dello stilo personalizzati all'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiamando il metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) . È possibile aggiungere dati dello stilo personalizzati alle code dell'oggetto **RealTimeStylus** in una delle tre posizioni seguenti.

-   Quando il parametro *queue* è impostato su **output**, i dati personalizzati vengono aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) dopo i dati attualmente elaborati dalla raccolta di plug-in sincrona.
-   Quando il parametro *queue* è impostato su **OutputImmediate**, i dati personalizzati vengono aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) prima che i dati vengano attualmente elaborati dalla raccolta di plug-in sincrona.
-   Quando il parametro *queue* è impostato su **input**, i dati personalizzati vengono aggiunti alla coda di input dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e inviati alla raccolta di plug-in sincrona prima dei nuovi dati del flusso di dati della penna del Tablet PC.

In ognuno dei casi precedenti, i dati aggiunti dai plug-in successivi nella raccolta di plug-in sincrono vengono aggiunti dopo i dati aggiunti dai plug-in precedenti.

> [!Note]  
> Se la chiamata al metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) viene eseguita da un plug-in sincrono in risposta a una chiamata a uno dei metodi [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) , i dati dello stilo personalizzati vengono aggiunti al flusso di dati della penna del tablet in modo prevedibile; in caso contrario, viene aggiunto alla coda in relazione ai dati di penna correnti che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) sta elaborando e non in relazione ai dati elaborati dal plug-in asincrono. Il metodo AddCustomStylusDataToQueue genera un'eccezione se l'oggetto **RealTimeStylus** è disabilitato.

 

I dati personalizzati dello stilo vengono aggiunti alla coda come oggetto [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) e i plug-in ricevono questi dati tramite il metodo [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. CustomStylusDataAdded](/previous-versions/ms824770(v=msdn.10)) .

Gli oggetti [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e [**GestureRecognizer**](gesturerecognizer-class.md) possono aggiungere dati dello stilo personalizzati alla coda. Per ulteriori informazioni sugli oggetti **DynamicRenderer** e **GestureRecognizer** , vedere plug-in di [renderer dinamici](dynamic-renderer-plug-ins.md) e [plug-](recognizer-plug-ins.md)in di riconoscimento.

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiama il metodo [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) sul thread dal quale riceve la chiamata al relativo metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) .

Il diagramma seguente illustra l'aggiunta di dati stilo personalizzati alla coda di output con il parametro *queue* impostato su **output**.

![illustrazione che mostra il flusso di dati stilo personalizzato nella coda di output ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

In questo diagramma i cerchi con lettera "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincroni. La lettera "C" del cerchio rappresenta i dati della penna del tablet che l'oggetto **RealTimeStylus** sta attualmente elaborando. Viene inviato alla raccolta di plug-in sincrono e inserito nella coda di output. I cerchi numerati "1", "2" e "3" rappresentano dati dello stilo personalizzati aggiunti alla coda di output rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono in risposta ai dati della penna del Tablet rappresentati da "C". I plug-in hanno aggiunto i dati dello stilo personalizzati con il parametro *queue* impostato su **StylusQueues**. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

Il diagramma seguente illustra l'aggiunta dei dati dello stilo personalizzati alla coda di output con il parametro *queue* impostato su **OutputImmediate**.

![Diagramma che mostra il flusso di dati stilo personalizzato nella coda di output.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

In questo diagramma i cerchi con lettera "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincroni. La lettera "C" del cerchio rappresenta i dati della penna del tablet che l'oggetto **RealTimeStylus** sta attualmente elaborando. Viene inviato alla raccolta di plug-in sincrono e inserito nella coda di output. I cerchi numerati "1", "2" e "3" rappresentano dati dello stilo personalizzati aggiunti alla coda di output rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono in risposta ai dati della penna del Tablet rappresentati da "C". I plug-in hanno aggiunto i dati dello stilo personalizzati con il parametro *queue* impostato su **OutputImmediate**. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

Il diagramma seguente illustra l'aggiunta di dati di stilo personalizzati alla coda di input.

![illustrazione che mostra il flusso di dati stilo personalizzato nella coda di output](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

In questo diagramma i cerchi con lettera "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincroni. La lettera "C" del cerchio rappresenta i dati della penna del tablet che l'oggetto **RealTimeStylus** sta attualmente elaborando. Viene inviato alla raccolta di plug-in sincrono e inserito nella coda di output. I cerchi numerati "1", "2" e "3" rappresentano dati dello stilo personalizzati aggiunti alla coda di input rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono in risposta ai dati della penna del tablet, rappresentati da "C". I plug-in hanno aggiunto i dati personalizzati dello stilo con il parametro *queue* impostato su **input**. I dati di stilo personalizzati numerati "1" vengono quindi passati ai plug-in sincroni e quindi alla coda di output prima dei dati dello stilo personalizzato numerati "2" e "3", entrambi elaborati prima dell'elaborazione dei successivi dati della penna del tablet. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

## <a name="error-data"></a>Dati errore

Quando un plug-in genera un'eccezione, il flusso di dati normale viene interrotto. L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) e chiama:

-   Il metodo [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) del plug-in che ha generato l'eccezione.
-   Metodo [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) dei rimanenti plug-in della raccolta.

Se il plug-in che ha generato l'eccezione è un plug-in sincrono, l'oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) viene aggiunto alla coda di output. Quindi, l'oggetto [**RealTimeStylus**](realtimestylus-class.md) riprende la normale elaborazione dei dati originali.

Il diagramma seguente illustra l'aggiunta dei dati degli errori ai dati della penna del Tablet PC.

![flusso di dati stilo personalizzato nella coda di output con l'aggiunta di dati di errore](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

In questo diagramma i cerchi con lettera "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincroni. La lettera "C" del cerchio rappresenta i dati della penna del tablet che l'oggetto **RealTimeStylus** sta attualmente elaborando. La lettera "e" del cerchio rappresenta un oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) generato dall'oggetto **RealTimeStylus** quando il secondo plug-in sincrono, ovvero un plug-in sincrono 2, genera un'eccezione durante l'elaborazione di "C". L'oggetto **RealTimeStylus** sospende quindi l'elaborazione di "C" e passa "e" al plug-in che ha generato l'eccezione e tutti i plug-in successivi. L'oggetto **RealTimeStylus** inserisce quindi "e" nella coda di output e riprende l'elaborazione di "C", che viene passata ai restanti plug-in nella raccolta di plug-in sincrona e posizionata nella coda di output dopo "e". Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

Se un plug-in genera un'eccezione dal relativo metodo Error, l'oggetto [**RealTimeStylus**](realtimestylus-class.md) intercetta l'eccezione, ma non genera un nuovo oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) . Per evitare la ricorsione.

I dati di errore vengono aggiunti alla coda di output dopo i dati di stilo personalizzati aggiunti nella posizione **OutputImmediate** prima dell'eccezione che ha creato i dati di errore e prima di tutti i dati dello stilo personalizzati aggiunti nella posizione **OutputImmediate** dai plug-in successivi nella raccolta di plug-in sincrona.

Il diagramma seguente illustra il modo in cui i dati di errore vengono aggiunti alla coda di output in relazione ai dati personalizzati aggiunti alla coda **OutputImmediate** .

![dati di errore aggiunti alla coda di output in relazione ai dati personalizzati aggiunti alla coda OutputImmediate.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

In questo diagramma i cerchi con lettera "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincroni. La lettera "C" del cerchio rappresenta i dati della penna del tablet che l'oggetto **RealTimeStylus** sta attualmente elaborando. I cerchi numerati "1", "2" e "3" vengono aggiunti rispettivamente dal primo, dal secondo e dal terzo plug-in sincrono alla coda **OutputImmediate** in risposta ai dati rappresentati dal cerchio con lettera "C". La lettera "e" del cerchio rappresenta i dati di errore generati in risposta a un'eccezione generata dal secondo plug-in dopo che il secondo plug-in ha aggiunto dati personalizzati alla coda di output nella posizione **OutputImmediate** .

Se un plug-in sincrono aggiunge dati di stilo personalizzati alla coda di input in risposta ai dati degli errori, i dati verranno aggiunti immediatamente prima dei dati di errore. Se uno qualsiasi dei plug-in sincroni aggiunge dati di stilo personalizzati alla coda di output nella posizione di **output** in risposta ai dati degli errori, i dati verranno aggiunti immediatamente dopo i dati di errore.

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiama il metodo [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) sul thread da cui viene generata l'eccezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Uso della classe RealTimeStylus](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
