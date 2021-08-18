---
description: Le API StylusInput consentono di interagire con il flusso di dati della penna del tablet. Per interagire con il flusso di dati, aggiungere un oggetto RealTimeStylus all'applicazione e aggiungere plug-in all'oggetto RealTimeStylus.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Architettura delle API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 961d6e3e94d47054afb28948685fce5fe1cafe9cbb0fa2f36e5a2d8508f28b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093160"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Architettura delle API StylusInput

Le API StylusInput consentono di interagire con il flusso di dati della penna del tablet. Per interagire con il flusso di dati, aggiungere un [**oggetto RealTimeStylus**](realtimestylus-class.md) all'applicazione e aggiungere plug-in all'oggetto **RealTimeStylus.**

Nelle API StylusInput sono disponibili due plug-in. [**L'oggetto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) implementa [**l'interfaccia IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) **L'oggetto DynamicRenderer** esegue il rendering dell'input penna in tempo reale, mentre viene disegnato. [**L'oggetto GestureRecognizer**](gesturerecognizer-class.md) implementa **le interfacce IStylusSyncPlugin** e [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) **L'oggetto GestureRecognizer** riconosce i movimenti dell'applicazione.

## <a name="definitions"></a>Definizioni

Nelle sezioni che descrivono le API StylusInput vengono usati i termini seguenti:

Plug-in sincrono

Classe che implementa [**l'interfaccia IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) I plug-in sincroni vengono in genere chiamati direttamente [**dall'oggetto RealTimeStylus.**](realtimestylus-class.md)

Plug-in asincrono

Classe che implementa [**l'interfaccia IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) I plug-in asincroni vengono in genere chiamati nel thread dell'interfaccia utente dell'applicazione.

Raccolta di plug-in sincroni

Raccolta [StylusSyncPluginCollection,](/previous-versions/ms824788(v=msdn.10)) ovvero una raccolta ordinata di [oggetti IStylusSyncPlugin.](/previous-versions/ms824751(v=msdn.10)) Una raccolta di plug-in sincrona in genere fa riferimento alla raccolta assegnata alla [proprietà SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) di un [oggetto RealTimeStylus.](/previous-versions/ms824830(v=msdn.10)) È possibile aggiungere solo plug-in sincroni a una raccolta di plug-in sincroni.

Raccolta di plug-in asincrona

Raccolta [StylusAsyncPluginCollection,](/previous-versions/ms824808(v=msdn.10)) ovvero una raccolta ordinata di [oggetti IStylusAsyncPlugin.](/previous-versions/ms824768(v=msdn.10)) Una raccolta di plug-in asincrona fa in genere riferimento alla raccolta assegnata alla [proprietà AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) di un [oggetto RealTimeStylus.](/previous-versions/ms824830(v=msdn.10)) È possibile aggiungere solo plug-in asincroni a una raccolta di plug-in asincroni.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Plug-in sincroni e asincroni

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) è progettato per fornire l'accesso in tempo reale al flusso di dati da una penna del tablet. Creare o usare plug-in sincroni per attività che richiedono l'accesso in tempo reale al flusso di dati e non vengono eseguite dal punto di vista del calcolo, ad esempio per il filtro dei pacchetti. Creare o usare plug-in asincroni per attività che non richiedono l'accesso in tempo reale al flusso di dati, ad esempio per la creazione e l'archiviazione di tratti in [**un oggetto InkDisp.**](inkdisp-class.md)

Alcune attività possono essere impegnative dal punto di vista del calcolo ma richiedono l'accesso in tempo reale al flusso di dati, ad esempio il riconoscimento dei movimenti a più sequenze. Per soddisfare queste esigenze, le API StylusInput forniscono un modello [**RealTimeStylus**](realtimestylus-class.md) a catena che consente di usare due **oggetti RealTimeStylus,** ognuno in esecuzione nel proprio thread. Per altre informazioni sul modello **RealTimeStylus** a catena, vedere [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

Per altre informazioni sull'uso e sulla creazione di plug-in, vedere [Uso delle API StylusInput](working-with-the-stylusinput-apis.md).

## <a name="the-tablet-pen-data-stream"></a>Flusso di dati della penna tablet

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) ha due code interne che trasportano i dati della penna del tablet, la coda di input e la coda di output. I dati della penna vengono convertiti in istanze delle classi nello spazio dei nomi [Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10)) L'elenco seguente descrive come **l'oggetto RealTimeStylus** gestisce i dati della penna del tablet:

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) controlla prima gli oggetti dati plug-in nella coda di input e quindi dal flusso di dati della penna del tablet.

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) invia un oggetto dati plug-in agli oggetti nella raccolta di plug-in sincrona. Ogni plug-in sincrono può aggiungere dati alla coda di input o di output.

Dopo che l'oggetto dati del plug-in è stato inviato a tutti i membri della raccolta di plug-in sincrona, l'oggetto dati del plug-in viene inserito nella coda di output dell'oggetto [**RealTimeStylus.**](realtimestylus-class.md)

[**L'oggetto RealTimeStylus**](realtimestylus-class.md) verifica quindi la presenza dell'oggetto dati del plug-in successivo da elaborare.

Mentre la coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) contiene dati, l'oggetto **RealTimeStylus** invia un oggetto dati plug-in dalla coda di output agli oggetti nella raccolta di plug-in asincrona. Ogni plug-in asincrono può aggiungere dati alla coda di input o di output. Tuttavia, poiché i plug-in asincroni vengono eseguiti nel thread dell'interfaccia utente, i dati vengono aggiunti alla coda in relazione ai dati penna correnti che l'oggetto **RealTimeStylus** sta elaborando e non in relazione ai dati che il plug-in asincrono sta elaborando.

Il diagramma seguente illustra il flusso dei dati della penna del tablet tramite [**l'oggetto RealTimeStylus**](realtimestylus-class.md) e le raccolte di plug-in.

![flusso dei dati della penna del tablet tramite l'oggetto realtimestylus e le raccolte di plug-in](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

In questo diagramma i cerchi etichettati "A" e "B" rappresentano i dati della penna del tablet già aggiunti alla coda di output dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e che non sono ancora stati inviati alla raccolta di plug-in asincrona. Il cerchio con etichetta "C" rappresenta i dati della penna del tablet che **l'oggetto RealTimeStylus** sta elaborando. Viene inviato alla raccolta di plug-in sincroni e inserito nella coda di output. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

Per altre informazioni sul modo in cui dati specifici vengono aggiunti alla coda ed elaborati, vedere [Dati plug-in e la classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>API StylusInput

Le API StylusInput si trovano principalmente negli spazi dei nomi [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) e [Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10)) Tuttavia, le API StylusInput fanno anche riferimento ad alcune classi nello spazio dei nomi [Microsoft.Ink,](/previous-versions/ms826516(v=msdn.10)) ad esempio la [classe Tablet,](/previous-versions/ms827783(v=msdn.10)) la raccolta [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) e le [enumerazioni ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) e [SystemGesture.](/previous-versions/ms827134(v=msdn.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**Realtimestylus**](realtimestylus-class.md)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[Uso delle API StylusInput](working-with-the-stylusinput-apis.md)
</dt> <dt>

[Modello RealTimeStylus a catena](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
