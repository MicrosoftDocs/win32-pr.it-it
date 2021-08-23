---
description: Un plug-in di riconoscimento è un oggetto che monitora il movimento della penna del tablet per individuare movimenti, grafia o altri oggetti.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Plug-in di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b64f8f9b63cdbdc7309e7d9bd303ecce7a6b59b2e3b3c0cde976d1d6eefdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091527"
---
# <a name="recognizer-plug-ins"></a>Plug-in di riconoscimento

Un plug-in di riconoscimento è un oggetto che monitora il movimento della penna del tablet per individuare movimenti, grafia o altri oggetti.

## <a name="system-gestures"></a>Movimenti di sistema

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) riconosce i movimenti di sistema. L'oggetto **RealTimeStylus** aggiunge un oggetto [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) alla coda [StylusQueues](/previous-versions/ms824786(v=msdn.10)) in risposta ai dati che completano il movimento, ad esempio un oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) per [SystemGesture.](/previous-versions/bb345349(v=vs.100)) Per altre informazioni, vedere [Dati plug-in e classe RealTimeStylus.](plug-in-data-and-the-realtimestylus-class.md)

## <a name="the-gesturerecognizer-object"></a>Oggetto GestureRecognizer

[**L'oggetto GestureRecognizer**](gesturerecognizer-class.md) implementa [**le interfacce IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) [**e IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) **L'oggetto GestureRecognizer** riconosce i movimenti dell'applicazione. Internamente, **l'oggetto GestureRecognizer** usa il riconoscimento movimenti Microsoft per eseguire il riconoscimento dei movimenti.

Quando [**l'oggetto GestureRecognizer**](gesturerecognizer-class.md) riconosce un movimento, aggiunge dati dello stilo personalizzati alla coda [StylusQueues](/previous-versions/ms824786(v=msdn.10)) in risposta [all'oggetto StylusUpData](/previous-versions/ms824057(v=msdn.10)) per il tratto. La proprietà [CustomDataId](/previous-versions/ms824748(v=msdn.10)) dell'oggetto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) è impostata sul valore [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) e la proprietà [Data](/previous-versions/ms824749(v=msdn.10)) dell'oggetto CustomStylusData contiene un oggetto [GestureRecognitionData.](/previous-versions/ms824594(v=msdn.10))

Il diagramma seguente illustra come [**l'oggetto GestureRecognizer**](gesturerecognizer-class.md) aggiunge dati ai dati della penna del tablet.

![illustrazione del flusso di dati gesturerecognizer](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

In questo diagramma il cerchio con lettera "SD" rappresenta un oggetto [StylusDownData](/previous-versions/ms824107(v=msdn.10)) e i cerchi con lettera "P" rappresentano gli oggetti [PacketsData](/previous-versions/ms824590(v=msdn.10)) che sono già stati aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. La lettera circolare "SU" rappresenta un [oggetto StylusUpData](/previous-versions/ms824057(v=msdn.10)) attualmente in elaborazione **dall'oggetto RealTimeStylus.** Viene inviato alla raccolta di plug-in sincroni e quindi inserito nella coda di output. I cerchi con lettera "GR" rappresentano i dati dello stilo personalizzati aggiunti alla coda di input dal plug-in [**GestureRecognizer**](gesturerecognizer-class.md) in risposta alla notifica dello stilo in alto associata a "SU". I dati dello stilo personalizzati con lettera "GR" vengono quindi passati ai plug-in sincroni e quindi alla coda di output prima dell'elaborazione dei dati della penna del tablet successivi. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i futuri dati della penna del tablet.

Per impostazione predefinita, [**l'oggetto GestureRecognizer**](gesturerecognizer-class.md) riconosce solo i movimenti a tratto singolo. Tuttavia, **l'oggetto GestureRecognizer** può essere impostato per riconoscere i movimenti a più sequenze. Per i movimenti a più sequenze, l'oggetto [CustomStylusData](/previous-versions/ms575208(v=vs.100)) viene aggiunto alla coda [StylusQueues](/previous-versions/ms824786(v=msdn.10)) in risposta all'oggetto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) per il tratto finale del movimento. Quando si riconoscono i movimenti a più sequenze, è possibile ricevere notifiche per set di tratti sovrapposti. Ad esempio, il primo e il secondo tratto insieme possono essere riconosciuti come un movimento e il secondo tratto da solo può essere riconosciuto come movimento. Per altre informazioni sul riconoscimento dei movimenti a più sequenze, vedere la **classe GestureRecognizer** e la [proprietà MaxStrokeCount.](/previous-versions/ms826053(v=msdn.10))

Se si usa l'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) per il riconoscimento del movimento a più sequenze, è possibile ottenere prestazioni ottimali usando un modello [**RealTimeStylus**](realtimestylus-class.md) a cascata e collegando l'oggetto **GestureRecognizer** all'oggetto **RealTimeStylus secondario.** Per altre informazioni sul modello **RealTimeStylus** a cascata, vedere [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Considerazioni speciali

L'elenco seguente descrive altri punti da considerare quando si usa [**l'oggetto GestureRecognizer.**](gesturerecognizer-class.md)

-   Non collegare un [**oggetto GestureRecognizer**](gesturerecognizer-class.md) a più oggetti [**RealTimeStylus.**](realtimestylus-class.md) Dopo aver **abilitato due oggetti RealTimeStylus** a cui è associato l'oggetto **GestureRecognizer,** si verifica quanto segue.
    -   [**L'oggetto GestureRecognizer**](gesturerecognizer-class.md) genera un'eccezione in risposta alla seconda chiamata al relativo metodo RealTimeStylusEnabled.
    -   Il secondo [**oggetto RealTimeStylus**](realtimestylus-class.md) abilitato genera un oggetto [ErrorData](/previous-versions/ms824740(v=msdn.10)) e notifica l'errore ai plug-in rimanenti nelle raccolte di plug-in.
    -   [**L'oggetto GestureRecognizer**](gesturerecognizer-class.md) interrompe il riconoscimento dei movimenti.
-   L'oggetto [**RealTimeStylus**](realtimestylus-class.md) genera un'eccezione quando viene chiamato il relativo metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) con il parametro *guid* impostato su [Microsoft.StylusInput.GestureRecognizer.GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) identificatore univoco globale (GUID).
-   L'oggetto [**GestureRecognizer**](gesturerecognizer-class.md) viene implementato come wrapper Component Object Model (COM) e non è possibile chiamare direttamente i relativi metodi di interfaccia [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Per altre informazioni sull'implementazione COM e [**sull'oggetto RealTimeStylus,**](realtimestylus-class.md) vedere Note sull'implementazione [per le API StylusInput.](implementation-notes-for-the-stylusinput-apis.md)

## <a name="custom-gesture-recognition"></a>Riconoscimento del movimento personalizzato

È possibile creare un plug-in di riconoscimento personalizzato che riconosca la grafia, i movimenti o altri oggetti:

-   Passaggio delle informazioni sul tratto a un oggetto [Recognizer](/previous-versions/ms829434(v=msdn.10)) esistente e uso del metodo [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) per aggiungere i risultati al flusso di dati della penna del tablet.
-   Esecuzione del riconoscimento all'interno del plug-in e uso del [metodo AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) per aggiungere i risultati al flusso di dati della penna del tablet.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti dell'applicazione](application-gestures.md)
</dt> <dt>

[Movimenti di sistema](system-gestures.md)
</dt> <dt>

[Sequenza temporale dei messaggi del mouse e degli eventi di sistema](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
