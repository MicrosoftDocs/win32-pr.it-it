---
description: Un plug-in di riconoscimento è un oggetto che monitora lo spostamento della penna del Tablet PC per un movimento, una grafia o altri oggetti.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Plug-in di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3ac866a211a78e2d8f347e89ca20a1906f436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568051"
---
# <a name="recognizer-plug-ins"></a>Plug-in di riconoscimento

Un plug-in di riconoscimento è un oggetto che monitora lo spostamento della penna del Tablet PC per un movimento, una grafia o altri oggetti.

## <a name="system-gestures"></a>Movimenti di sistema

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) riconosce i movimenti di sistema. L'oggetto **RealTimeStylus** aggiunge un oggetto [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) alla coda [StylusQueues](/previous-versions/ms824786(v=msdn.10)) in risposta ai dati che completano il movimento, ad esempio un oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) per [SystemGesture](/previous-versions/bb345349(v=vs.100)). Per altre informazioni, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>Oggetto GestureRecognizer

L'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) implementa le interfacce [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . L'oggetto **GestureRecognizer** riconosce i movimenti dell'applicazione. Internamente, l'oggetto **GestureRecognizer** usa il riconoscitore di movimento Microsoft per eseguire il riconoscimento dei movimenti.

Quando l'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) riconosce un movimento, aggiunge dati dello stilo personalizzati alla coda [StylusQueues](/previous-versions/ms824786(v=msdn.10)) in risposta all'oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) per il tratto. La proprietà [CustomDataId](/previous-versions/ms824748(v=msdn.10)) dell'oggetto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) è impostata sul valore [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) e la proprietà [dati](/previous-versions/ms824749(v=msdn.10)) dell'oggetto CustomStylusData contiene un oggetto [GestureRecognitionData](/previous-versions/ms824594(v=msdn.10)) .

Il diagramma seguente illustra il modo in cui l'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) aggiunge dati ai dati della penna del tablet.

![illustrazione del flusso di dati GestureRecognizer](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

In questo diagramma il cerchio con lettera "SD" rappresenta un oggetto [StylusDownData](/previous-versions/ms824107(v=msdn.10)) e i cerchi con lettera "P" rappresentano gli oggetti [PacketsData](/previous-versions/ms824590(v=msdn.10)) che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. Il cerchio con lettera "SU" rappresenta un oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) che l'oggetto **RealTimeStylus** sta attualmente elaborando. Viene inviato alla raccolta di plug-in sincrono e quindi inserito nella coda di output. I cerchi con lettera "GR" rappresentano i dati dello stilo personalizzati aggiunti alla coda di input dal plug-in [**GestureRecognizer**](gesturerecognizer-class.md) in risposta alla notifica dello stilo in alto associata a "su". I dati di stilo personalizzati con lettera "GR" vengono quindi passati ai plug-in sincroni e quindi alla coda di output prima dell'elaborazione dei successivi dati della penna del tablet. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

Per impostazione predefinita, l'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) riconosce solo i movimenti a tratto singolo; Tuttavia, l'oggetto **GestureRecognizer** può essere impostato per riconoscere i movimenti a più tratti. Per i movimenti a più tratti, l'oggetto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) viene aggiunto alla coda [StylusQueues](/previous-versions/ms824786(v=msdn.10)) in risposta all'oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) per il tratto finale del movimento. Quando si riconoscono i movimenti a più sequenze, è possibile ricevere notifiche per set di tratti sovrapposti. Ad esempio, il primo e il secondo tratto possono essere riconosciuti come un unico gesto e il secondo tratto può essere riconosciuto come un movimento. Per ulteriori informazioni sul riconoscimento dei movimenti a più sequenze, vedere la classe **GestureRecognizer** e la proprietà [MaxStrokeCount](/previous-versions/ms826053(v=msdn.10)) .

Se si utilizza l'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) per il riconoscimento dei movimenti a più sequenze, è possibile ottenere prestazioni ottimali utilizzando un modello [**RealTimeStylus**](realtimestylus-class.md) a cascata e alleghiendo l'oggetto **GestureRecognizer** all'oggetto **RealTimeStylus** secondario. Per ulteriori informazioni sul modello **RealTimeStylus** a cascata, vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Considerazioni speciali

Nell'elenco seguente vengono descritti altri punti da considerare quando si usa l'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) .

-   Non è consigliabile alleghi un oggetto [**GestureRecognizer**](gesturerecognizer-class.md) a più di un oggetto [**RealTimeStylus**](realtimestylus-class.md) . Quando due oggetti **RealTimeStylus** a cui è collegato l'oggetto **GestureRecognizer** sono abilitati, si verifica quanto segue.
    -   L'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) genera un'eccezione in risposta alla seconda chiamata al metodo RealTimeStylusEnabled.
    -   Il secondo oggetto [**RealTimeStylus**](realtimestylus-class.md) abilitato genera un oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) e notifica ai rimanenti plug-in le raccolte di plug-in dell'errore.
    -   L'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) interrompe il riconoscimento dei movimenti.
-   L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione quando viene chiamato il metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) con il parametro *GUID* impostato sull'identificatore univoco globale (Guid) [Microsoft. StylusInput. GestureRecognizer. GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) .
-   L'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) viene implementato come wrapper Component Object Model (com) e non è possibile chiamare direttamente i metodi di interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Per ulteriori informazioni sull'implementazione COM e sull'oggetto [**RealTimeStylus**](realtimestylus-class.md) , vedere [Note sull'implementazione per le API StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-gesture-recognition"></a>Riconoscimento di movimenti personalizzati

È possibile creare un plug-in di riconoscimento personalizzato che riconosce la grafia, i movimenti o altri oggetti da:

-   Passaggio delle informazioni sul tratto a un oggetto [Recognizer](/previous-versions/ms829434(v=msdn.10)) esistente e utilizzo del metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) per aggiungere i risultati al flusso dei dati della penna del tablet.
-   Esecuzione del riconoscimento all'interno del plug-in e utilizzo del metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) per aggiungere i risultati al flusso di dati della penna del tablet.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti dell'applicazione](application-gestures.md)
</dt> <dt>

[Movimenti di sistema](system-gestures.md)
</dt> <dt>

[Sequenza temporale dei messaggi del mouse e degli eventi di sistema](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
