---
title: Creare ed eseguire l'esempio StoClien
description: StoClien funziona in collaborazione con un oggetto della carta in un server COM per ottenere l'archiviazione persistente dei disegni nei file composti COM.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Creare ed eseguire l'esempio StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f00274293c05e21e660dc8e9448ca95946cab8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298070"
---
# <a name="create-and-run-stoclien-sample"></a>Creare ed eseguire l'esempio StoClien

**StoClien** funziona in collaborazione con un oggetto della carta in un server com per ottenere l'archiviazione persistente dei disegni nei file composti com. Per ulteriori informazioni sull'utilizzo dei flussi nel file composto fornito da **StoClien**, vedere l'esempio [**StoServe**](structured-storage-server-sample--stoserve-.md) e STOSERVE.HTM. La costruzione della cocarta e la relativa interfaccia IPaper sono descritte anche nell'esempio **StoServe** .

## <a name="code-tour"></a>Tour del codice

Gli argomenti principali trattati in questa presentazione del codice sono:

-   Come **CGuiPaper** incapsula il comportamento dell'interfaccia utente grafica del documento di disegno elettronico di **StoClien**
-   Come **StoClien** acquisisce e visualizza l'attività di disegno interattivo
-   Modalità di utilizzo del documento da parte dell'oggetto **CGuiPaper** per registrare i dati di disegno
-   Modalità di utilizzo di una connessione IPaperSink nella ridisegno
-   Come i metodi **Load** e **Save** di CPapFile usano l'archiviazione strutturata nei file composti

Poiché la classe **CGuiBall** utilizzata negli esempi FRECLIEN e CONCLIEN incapsula il comportamento di una palla da rimbalzo, **StoClien** utilizza una classe C++ **CGuiPaper** per incapsulare i dati e il comportamento dell'interfaccia utente grafica del documento di disegno elettronico.

La tabella seguente elenca i file pertinenti per l'esempio **StoClien** .



| File        | Descrizione                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Breve descrizione di esempio.                                                                                                        |
| MAKEFILE     | Il makefile generico per la compilazione dell'esempio di codice.                                                                               |
| STOCLIEN. H   | File di inclusione per l'applicazione **StoClien** . Contiene le dichiarazioni di classe, i prototipi di funzione e gli identificatori di risorsa.   |
| STOCLIEN. CPP | File di implementazione principale per STOCLIEN.EXE. Dispone dell'implementazione di WinMain e CMainWindow, nonché dell'invio del menu principale. |
| STOCLIEN. RC  | Il file di definizione della risorsa dell'applicazione.                                                                                        |
| STOCLIEN. ICO | Risorsa icona dell'applicazione.                                                                                                   |
| STOCLIEN. PAP | Un file di disegno cartaceo predefinito per l'applicazione.                                                                                |
| Matita. CUR   | Immagine a matita per il cursore della finestra client.                                                                                     |
| SINK. H       | Dichiarazione di classe per la classe di oggetti COM COPaperSink.                                                                      |
| SINK. CPP     | File di implementazione per la classe di oggetti COM COPaperSink.                                                                        |
| PAPFILE. H    | Dichiarazione di classe per la classe C++ **CPapFile** .                                                                            |
| PAPFILE. CPP  | File di implementazione per la classe C++ **CPapFile** .                                                                              |
| GUIPAPER. H   | Dichiarazione di classe per la classe C++ **CGuiPaper** .                                                                           |
| GUIPAPER. CPP | File di implementazione per la classe C++ **CGuiPaper** .                                                                             |
| STOCLIEN. DSP | Microsoft Visual Studio file di progetto.                                                                                            |



 

## <a name="compound-files"></a>file compositi

**StoClien** si basa sulla cocarta per registrare i dati di disegno. Si basa inoltre sulla cocarta per archiviare i dati in un file composto. Tuttavia, in una tipica divisione del lavoro tra client e server COM, **StoClien** condivide parte della responsabilità per l'archiviazione di file. Questa divisione del lavoro è importante nelle applicazioni COM in cui il client è un contenitore e il server è un oggetto incorporato. In questo accordo, il client è responsabile della creazione o dell'apertura di un file di archiviazione strutturata, mentre l'oggetto server è responsabile dell'uso di tale archiviazione per scopi di archiviazione dei dati propri. Questo può comportare l'oggetto server che crea le sottoarchiviazioni nello spazio di archiviazione fornito. In genere, l'oggetto server crea oggetti flusso nell'archivio. L'uso dei flussi di archiviazione da parte di un documento è dettagliato nell'esempio **StoClien** .

L'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) viene utilizzata sia dal client che dall'oggetto server per eseguire operazioni sui file. Viene usata l'implementazione dei file composti dell'architettura di archiviazione strutturata. Le funzioni di servizio standard vengono utilizzate per le operazioni sui file composti. Ad esempio, la funzione [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) crea inizialmente un file composto e passa di nuovo un puntatore **IStorage** che può essere usato per modificare il file. Questa particolare funzione viene chiamata in **StoClien**. L'interfaccia **IStorage** ottenuta viene passata come parametro a un documento per l'utilizzo. L'oggetto Copaper non crea né apre i file composti in modo autonomo: usa le interfacce **IStorage** e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per lavorare nei file composti che vi sono assegnati.

Queste interfacce [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) non sono implementate all'interno di **StoClien** o **StoServe**. Vengono implementate all'interno delle librerie COM. Quando viene ottenuto un puntatore a una di queste interfacce, i relativi metodi vengono essenzialmente usati come set di servizi per operare su un file composto.

 

 




