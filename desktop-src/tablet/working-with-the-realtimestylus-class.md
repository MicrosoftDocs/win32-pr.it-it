---
description: La classe RealTimeStylus fa parte delle API (Application Programming Interface) di StylusInput. Le sezioni seguenti descrivono gli elementi chiave della classe RealTimeStylus e le API StylusInput.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Uso della classe RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 919c4de38cb0835996928c877ca4c42faf6a5f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752431"
---
# <a name="working-with-the-realtimestylus-class"></a>Uso della classe RealTimeStylus

La classe [**RealTimeStylus**](realtimestylus-class.md) fa parte delle API (Application Programming Interface) di StylusInput. Le sezioni seguenti descrivono gli elementi chiave della classe **RealTimeStylus** e le API StylusInput.

## <a name="instantiating-the-realtimestylus-class"></a>Creazione di un'istanza della classe RealTimeStylus

Quando si crea un oggetto [**RealTimeStylus**](realtimestylus-class.md) , è possibile collegarlo a un handle di finestra o a un controllo. Per il fissaggio dell'oggetto **RealTimeStylus** a un handle di finestra sono necessarie autorizzazioni aggiuntive. Per altre informazioni su queste autorizzazioni, vedere [considerazioni relative all'attendibilità parziale per le API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> Non è possibile aggiungere l'oggetto [**RealTimeStylus**](realtimestylus-class.md) a una finestra o a un controllo in un processo diverso.

 

Se si usa il costruttore predefinito, si crea un oggetto [**RealTimeStylus**](realtimestylus-class.md) che può accettare solo input da un altro oggetto **RealTimeStylus** . Per ulteriori informazioni sulla connessione di due oggetti **RealTimeStylus** , vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) implementa l'interfaccia [IDisposable](/dotnet/api/system.idisposable) .

## <a name="extending-the-realtimestylus-class"></a>Estensione della classe RealTimeStylus

Per consentire ai plug-in di interagire con il flusso di dati dalla penna del tablet, l'oggetto [**RealTimeStylus**](realtimestylus-class.md) gestisce due raccolte di plug-in, accessibili dai metodi [**GetStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) e [**GetStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) in C++ e dalle proprietà [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) e [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) nel codice gestito. È possibile aggiungere un plug-in chiamando il metodo [**AddStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) o [**AddStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) della raccolta all'interno della proprietà appropriata. Per altre informazioni sulla creazione e sull'uso dei plug-in, vedere [plug-in e la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md). Per informazioni su come decidere se creare un plug-in sincrono o asincrono per una particolare attività, vedere [considerazioni relative al threading per le API di StylusInput](threading-considerations-for-the-stylusinput-apis.md) e [considerazioni sulle prestazioni per le API StylusInput](performance-considerations-for-the-stylusinput-apis.md).

I plug-in sincroni devono implementare l'interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ed è necessario che i plug-in asincroni implementino l'interfaccia [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Ogni plug-in ha una proprietà [**IStylusSyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) o [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) . L'oggetto [**RealTimeStylus**](realtimestylus-class.md) chiama solo i metodi di notifica del plug-in per i metodi in cui è stato sottoscritto il plug-in. Per ulteriori informazioni sui metodi di notifica, vedere la pagina relativa ai [dati plug-in e alla classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) implementa l'interfaccia [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . L'unico modo per creare un'istanza di un oggetto **RealTimeStylus** che accetta input da un altro oggetto **RealTimeStylus** consiste nell'usare il costruttore predefinito e implementare il modello **RealTimeStylus** a cascata. Per ulteriori informazioni sulla connessione di due oggetti **RealTimeStylus** , vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) dispone di due code interne che contengono i dati della penna del tablet, la coda di input e la coda di output. I dati della penna vengono convertiti in istanze delle classi nello spazio dei nomi [Microsoft. StylusInput. PluginData](/previous-versions/ms574862(v=vs.100)) . Nell'elenco seguente viene descritto il modo in cui l'oggetto **RealTimeStylus** gestisce i dati della penna del tablet.

1.  L'oggetto [**RealTimeStylus**](realtimestylus-class.md) verifica innanzitutto la presenza di oggetti dati plug-in nella coda di input e quindi dal flusso di dati della penna del tablet.
2.  L'oggetto [**RealTimeStylus**](realtimestylus-class.md) Invia un oggetto dati plug-in agli oggetti nella relativa raccolta di plug-in sincrona. Ogni plug-in sincrono può aggiungere dati alla coda di input o di output.
3.  Una volta che l'oggetto dati del plug-in è stato inviato a tutti i membri della raccolta di plug-in sincrono, l'oggetto dati del plug-in viene inserito nella coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) .
4.  L'oggetto [**RealTimeStylus**](realtimestylus-class.md) verifica quindi la presenza del successivo oggetto dati plug-in da elaborare.
5.  Mentre la coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) contiene dati, l'oggetto **RealTimeStylus** Invia un oggetto dati plug-in dalla relativa coda di output agli oggetti nella relativa raccolta di plug-in asincroni. Ogni plug-in asincrono può aggiungere dati alla coda di input o di output, ma dal momento che i plug-in asincroni vengono eseguiti nel thread dell'interfaccia utente, i dati vengono aggiunti alla coda in relazione ai dati penna correnti che l'oggetto **RealTimeStylus** sta elaborando e non in relazione ai dati elaborati dal plug-in asincrono.

Il diagramma seguente illustra il flusso dei dati della penna del Tablet PC tramite l'oggetto [**RealTimeStylus**](realtimestylus-class.md) e le relative raccolte di plug-in.

![illustratiom visualizzazione del flusso di dati della penna del Tablet PC](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

In questo diagramma i cerchi con lettera "A" e "B" rappresentano i dati della penna del tablet che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincroni. La lettera "C" del cerchio rappresenta i dati della penna del tablet che l'oggetto **RealTimeStylus** sta attualmente elaborando. Viene inviato alla raccolta di plug-in sincrono e inserito nella coda di output. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

Per ulteriori informazioni sull'aggiunta e l'elaborazione di dati specifici nella coda, vedere la pagina relativa [ai dati dei plug-in e alla classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Di seguito è riportato uno scenario minimo per l'utilizzo dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) in un modulo che raccoglie l'input penna.

1.  Creare un form che implementi l'interfaccia [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Creare un oggetto [**RealTimeStylus**](realtimestylus-class.md) associato a un controllo nel form.
3.  Impostare interesse per le notifiche StylusDown, pacchetti e StylusUp nella proprietà [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) del modulo.
4.  Nei metodi [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)e [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del modulo, aggiungere il codice per gestire lo stilo, i pacchetti e le notifiche dello stilo, che vengono inviati dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) del modulo.

Per un esempio di tale applicazione, vedere l' [esempio RealTimeStylus Ink Collection](realtimestylus-ink-collection-sample.md).

## <a name="working-with-tablet-objects"></a>Utilizzo di oggetti Tablet

Ogni oggetto [**RealTimeStylus**](realtimestylus-class.md) abilitato gestisce un elenco di identificatori univoci per gli oggetti [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) con cui può interagire. L'oggetto **RealTimeStylus** espone due metodi per la conversione tra l'identificatore univoco e l'oggetto **Tablet** , ovvero i metodi [**GetTabletContextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) e [**GetTabletFromTabletContextId**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid) .

L'oggetto [TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) (in codice gestito) contiene una proprietà [PacketPropertyId](/previous-versions/ms827780(v=msdn.10)) e una struttura [TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) che descrive l'intervallo, la risoluzione e le unità della proprietà per un oggetto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) specifico. Il metodo [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) restituisce una matrice di identificatori univoci globali (Guid) per le proprietà del pacchetto che l'oggetto **RealTimeStylus** invia ai relativi plug-in quando tali proprietà sono disponibili. Per modificare il set di proprietà dei pacchetti che l'oggetto **RealTimeStylus** passa ai relativi plug-in, chiamare il metodo [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) dell'oggetto **RealTimeStylus** . Il metodo [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (nel codice gestito) dell'oggetto **RealTimeStylus** accetta un identificatore di Tablet univoco e restituisce una raccolta di oggetti [TabletPropertyDescription](/previous-versions/ms827760(v=msdn.10)) . Queste proprietà del pacchetto rappresentano il subset di proprietà supportate dal tablet restituito dal metodo **GetDesiredPacketDescription** .

Per un elenco dei GUID della proprietà del pacchetto standard, vedere la classe delle [costanti PacketPropertyGuids](packetpropertyguids-constants.md) .

## <a name="special-considerations"></a>Considerazioni speciali

Nell'elenco seguente vengono descritti altri punti da considerare quando si usa l'oggetto [**RealTimeStylus**](realtimestylus-class.md) con un oggetto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

-   Il metodo [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) può essere chiamato solo quando l'oggetto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) è disabilitato. L'oggetto [**RealTimeStylus**](realtimestylus-class.md) può modificare l'elenco delle proprietà dei pacchetti desiderate. quindi, chiamare il metodo [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) dopo la chiamata al metodo **SetDesiredPacketDescription** per determinare le proprietà dei pacchetti che l'oggetto **RealTimeStylus** può inviare ai relativi plug-in. Un tablet è garantito solo per supportare i valori **X**, **Y** e **PacketStatus** per l'oggetto [PacketProperty](packetproperty-guids.md). Pertanto, potrebbe essere necessario che la progettazione del plug-in tenga conto della ricezione di un minor numero di proprietà del pacchetto.
-   Il metodo [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (per il codice gestito) può essere chiamato solo quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato. Poiché è possibile inviare una notifica ai plug-in asincroni dopo che l'oggetto **RealTimeStylus** è stato disabilitato, potrebbe essere necessario memorizzare nella cache le informazioni per ogni oggetto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Il metodo GetTabletPropertyDescriptionCollection restituisce un elenco delle proprietà dei pacchetti desiderate supportate dal Tablet specificato.
-   Quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md) è abilitato, ogni plug-in riceve una chiamata al metodo [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) . L'oggetto [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10)) passato nella notifica contiene una raccolta di identificatori di contesto per le tavolette disponibili nel momento in cui l'oggetto **RealTimeStylus** è abilitato.
-   Quando un tablet che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) può utilizzare viene aggiunto o rimosso dal Tablet PC mentre l'oggetto **RealTimeStylus** è abilitato, l'oggetto **RealTimeStylus** notifica ai plug-in che un oggetto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) è stato aggiunto o rimosso. Per altre informazioni, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Utilizzo delle penne del Tablet

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) passa informazioni sulla penna del Tablet ai relativi plug-in in una serie di metodi di notifica. Le informazioni sulla penna del tablet sono rappresentate da un oggetto [stilo](/previous-versions/ms824824(v=msdn.10)) , ottenute tramite il metodo [**getstiles**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) . Questo oggetto è una rappresentazione della penna del Tablet nel momento in cui sono stati raccolti i dati. Poiché i plug-in ricevono i dati della penna del tablet come parte del flusso di dati della penna del tablet, i plug-in devono usare le informazioni nell'oggetto stilo anziché controllare lo stato corrente di una particolare penna del tablet tramite la classe [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Per informazioni su come vengono passati i dati dei pulsanti Tablet Pen e Tablet Pen ai plug-in, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Per ottenere una matrice degli oggetti [stilo](/previous-versions/ms824824(v=msdn.10)) rilevati dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) dall'ultima abilitazione, utilizzare il metodo [**getstiles**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) dell'oggetto **RealTimeStylus** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[Modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Considerazioni sull'attendibilità parziale per le API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
