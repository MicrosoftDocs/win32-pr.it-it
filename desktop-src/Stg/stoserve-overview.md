---
title: Panoramica di StoServe
description: Nell'esempio di codice StoServe viene illustrato come utilizzare i servizi di archiviazione strutturati come fornito nell'implementazione dei file composti. Viene descritto l'uso delle interfacce IStorage e IStream standard.
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338535"
---
# <a name="stoserve-overview"></a>Panoramica di StoServe

## <a name="purpose"></a>Scopo

L'obiettivo principale di questo esempio di codice è l'uso di servizi di archiviazione strutturati come fornito nell'implementazione dei file composti. Viene descritto l'uso delle interfacce [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) standard. **StoServe** funziona con l'esempio di codice [StoClien](structured-storage-client-sample--stoclien-.md) per illustrare l'uso combinato dell'archiviazione di file composti per client e server.

## <a name="functionality"></a>Funzionalità

Nell'esempio **StoServe** viene introdotto l'oggetto com di un documento, che rappresenta virtualmente un foglio di disegno vuoto.

Gli oggetti Copaper espongono un set di funzionalità per il disegno in formato libero sull'area della carta utilizzando "Ink" del colore e della larghezza specificati. La funzionalità è esternamente simile agli esempi di esercitazione "Scribble" in molte versioni di Microsoft Visual C++. La differenza tra gli  / esempi **StoClien** di StoServe è un'architettura basata principalmente sulla tecnologia com. Le funzionalità della carta di disegno elettronica degli oggetti della carta sono disponibili per i client tramite un'interfaccia [**iPaper**](ipaper-methods.md) personalizzata. Il Copaper implementa l'interfaccia **iPaper** . Una chiara distinzione architetturale viene mantenuta tra client e server. Non viene fornita alcuna interfaccia utente grafica (GUI) da un foglio di lavoro. La progettazione dell'oggetto Copaper si basa sul client per tutto il comportamento dell'interfaccia utente grafica. Il Copaper incapsula solo l'acquisizione e l'archiviazione basate su server dei dati Ink creati.

I dati dell'input penna disegnati sulla superficie della cocarta possono essere archiviati e caricati da file composti. I metodi [**iPaper**](ipaper-methods.md), [**Save**](ipaper--save.md) e [**Load**](ipaper--load.md) accettano un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Il Copaper usa questa interfaccia **IStorage** fornita dal client per archiviare i dati di disegno.

Il documento è ospitato in un server in-process e reso disponibile pubblicamente come componente COM personalizzato. Analogamente ad altri server in questa serie di esercitazioni, StoServe è un server COM con registrazione automatica. Rende disponibile il tipo di oggetto Copaper ai client come componente DllPaper usando una \_ registrazione DLLPAPER CLSID nel registro di sistema.

Come nel server di conservazione precedente, le funzionalità degli oggetti collegabili sono supportate in un documento. L'interfaccia [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) viene esposta e viene implementato un punto di connessione appropriato. In questo contesto, un'interfaccia IPaperSink personalizzata in uscita viene dichiarata per l'uso nell'invio di notifiche al client.

Le due interfacce personalizzate [**iPaper**](ipaper-methods.md) e [**IPaperSink**](ipapersink-methods.md) sono dichiarate in iPaper. H che si trova nella directory comune di pari livello \\ Inc. I GUID per le interfacce e gli oggetti sono definiti in PAPGUIDS. H che si trova nella stessa directory di inclusione comune.

La funzionalità CThreaded in APPUTIL viene usata da **StoServe** per ottenere thread safety, come nell'esempio Freserve. Gli oggetti della cocarta sono derivati dalla classe CThreaded e ereditano i relativi metodi OwnThis e UnOwnThis. Questi metodi consentono a un solo thread alla volta di accedere al server **StoServe** e agli oggetti di Copaper gestiti dal server.

## <a name="copaper-com-object"></a>Oggetto COM della cocarta

L'oggetto COM della cocarta è il singolo tipo di oggetto gestito da questo server **StoServe** in-process. Il Copaper viene costruito come oggetto COM collegabile con un'implementazione dell'interfaccia [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) standard e un'implementazione dell'interfaccia [**iPaper**](ipaper-methods.md) personalizzata. Il Copaper espone l'interfaccia **iPaper** in modo che i client possano eseguire un piccolo set di operazioni di carta elettronica su un'istanza di Copaper. Le operazioni essenziali avviano una sequenza di disegno dell'input penna, disegnano i dati dell'input penna sull'area della carta virtuale del documento e terminano la sequenza di disegno dell'input penna. In questo schema, si presuppone che il client sia un'applicazione GUI basata su un mouse o un dispositivo tablet. Il client è responsabile della conversione dei movimenti del mouse in richieste a un documento, che consente di salvare tali richieste come dati di input penna.

Sono disponibili due livelli di salvataggio dei dati di input penna in un documento. Il documento salva i dati di input penna in una matrice basata su RAM che rappresenta il disegno corrente e il Copaper Salva in modo permanente un intero disegno in un file composto. I metodi nell'interfaccia [**iPaper**](ipaper-methods.md) eseguono entrambi.

Poiché il client non gestisce i dati cartacei disegnati, ma è responsabile del rendering come immagine sullo schermo, l'implementazione di [**iPaper**](ipaper-methods.md) in un documento deve esporre un metodo che consenta al client di ottenere i dati di disegno. A questo scopo, viene usata la tecnologia degli oggetti collegabile in un documento. Un \_ punto di connessione PAPERSINK di CONNPOINT viene implementato da un foglio di lavoro in modo che un client possa connettersi a un documento per ricevere i dati di input penna per il disegno. Il client chiama prima il metodo [iPaper:: Redraw](ipaper--redraw.md) nell'oggetto Copaper per richiedere tutti i dati di input penna del disegno corrente. L'implementazione della cocarta di ridisegni usa quindi l'implementazione client di [**IPaperSink**](ipapersink-methods.md) per passare i dati al client.

Quando l'utente disegna in modo interattivo il client, disegna i dati immediatamente sullo schermo e li invia al documento per il salvataggio. Quando il client richiede che lo schermo venga ridisegnato, viene chiamato il metodo di [ridisegno](ipaper--redraw.md) del Copaper. Questo tipo di ridisegno è comune nelle applicazioni. Ad esempio, il ridisegno si verifica quando la finestra del client viene sovrapposta da un'altra finestra dell'applicazione. Il client dispone di un rendering bitmap dell'immagine disegnata, ma la bitmap è facilmente persa e spesso deve essere ridisegnata. Il client si basa su un documento nel server per i dati di input penna necessari per il ridisegno.

Si tratta di una divisione client/server comune del lavoro. È particolarmente appropriato quando è necessario che più client condividano i dati. Il documento è codificato per consentire questo problema. Usa la funzionalità APPUTIL CThreaded per ottenere thread safety. Un'applicazione che potrebbe sfruttare questo progetto è un'applicazione lavagna condivisa, in cui più client possono contribuire a un disegno comunemente visualizzato. Il supporto COM per Distributed COM (DCOM) supporta questo tipo di utilizzo dell'applicazione del gruppo di lavoro in rete. Per ulteriori informazioni, vedere l'esempio precedente di REMCLIEN.

Un uso più modesto dello schema client/server di Copaper consiste nell'integrare il comportamento per gli oggetti implementati in applicazioni diverse nello stesso computer. In questo caso, è possibile che i client siano un contenitore ActiveX in applicazioni separate che condividono i dati gestiti dallo stesso oggetto. Questi dati potrebbero non essere i dati di disegno dell'input penna supportati dal componente DllPaper. **StoServe** può essere usato come Framework di avvio per la programmazione di componenti che gestiscono altri tipi di dati condivisi.

## <a name="support-information"></a>Informazioni relative al supporto

Il makefile **StoServe** registra il componente com DllPaper **StoServe** nel registro di sistema. Questo componente deve essere registrato prima che **StoServe** sia disponibile all'esterno dei client com come server per tale componente. Questa registrazione automatica viene eseguita utilizzando l'utilità Register.exe incorporata nell'esempio di registrazione. Per compilare o eseguire **StoServe**, compilare innanzitutto l'esempio di codice Register.

Per ulteriori informazioni sulla configurazione del sistema per compilare e testare gli esempi di codice in questa serie di esercitazioni COM, vedere [How to Build Samples](how-to-build-samples.md). Il Makefile fornito è compatibile con Microsoft NMAKE. Per creare una build di debug, eseguire il comando NMAKE nella finestra del prompt dei comandi.

Per un uso pratico in Microsoft Visual Studio, viene fornito un file di progetto per ogni esempio. Per caricare il progetto per l'esempio **StoServe** , è possibile eseguire Visual Studio al prompt dei comandi nella directory Samples come indicato di seguito:

STOSERVE MSDEV. DSP

È anche possibile fare doppio clic sul file stoserve. DSP in Esplora risorse per caricare un progetto di esempio in Visual Studio. In Visual Studio è possibile esplorare le classi C++ dell'origine di esempio e in genere eseguire le altre operazioni di modifica-compilazione-debug.

> [!Note]  
> Nell'ambito del Software Development Kit (SDK) della piattaforma, la compilazione di questi esempi da Visual Studio richiede l'impostazione appropriata dei percorsi di directory in Visual Studio. Per ulteriori informazioni, vedere [How to Build Samples](how-to-build-samples.md).

 

 

 