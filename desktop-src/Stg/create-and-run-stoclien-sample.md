---
title: Creare ed eseguire l'esempio StoClien
description: StoClien opera in collaborazione con un oggetto COPaper in un server COM per ottenere l'archiviazione permanente dei disegni nei file composti COM.
ms.assetid: bf622104-10dd-4649-88f0-e2bfb15289b1
keywords:
- Creare ed eseguire l'esempio StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3d9526e81fc3fb2d6a0cfb03e8943ccf68688096588122da87861d8c88e531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663461"
---
# <a name="create-and-run-stoclien-sample"></a>Creare ed eseguire l'esempio StoClien

**StoClien opera** in collaborazione con un oggetto COPaper in un server COM per ottenere l'archiviazione permanente dei disegni nei file composti COM. Per altre informazioni sull'uso dei flussi da parte di COPaper nel file composto fornito a COPaper da **StoClien,** vedere l'esempio [**StoServe**](structured-storage-server-sample--stoserve-.md) STOSERVE.HTM. La costruzione di COPaper e la relativa interfaccia IPaper sono trattate anche **nell'esempio StoServe.**

## <a name="code-tour"></a>Presentazione del codice

Gli argomenti principali trattati in questa presentazione del codice sono:

-   In **che modo CGuiPaper** incapsula il comportamento dell'interfaccia utente grafica della carta da disegno elettronica di **StoClien**
-   Come **StoClien acquisisce** e visualizza l'attività di disegno interattiva
-   Come **l'oggetto CGuiPaper** usa COPaper per registrare i dati di disegno
-   Come viene usata una connessione IPaperSink per ridisegnare
-   Come i metodi CPapFile **Load** e **Save** usano l'archiviazione strutturata nei file composti

Poiché la classe **CGuiBall** usata negli esempi FRECLIEN e CONCLIEN incapsula il comportamento di una palla da disegno, **StoClien** usa una **classe CGuiPaper** C++ per incapsulare i dati e il comportamento dell'interfaccia utente grafica della carta da disegno elettronica.

Nella tabella seguente sono elencati i file pertinenti **all'esempio StoClien.**



| File        | Descrizione                                                                                                                      |
|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| STOCLIEN.TXT | Breve descrizione di esempio.                                                                                                        |
| Makefile     | Makefile generico per la compilazione dell'esempio di codice.                                                                               |
| STOCLIEN. H   | File di inclusione per **l'applicazione StoClien.** Contiene dichiarazioni di classe, prototipi di funzione e identificatori di risorsa.   |
| STOCLIEN. CPP | File di implementazione principale per STOCLIEN.EXE. Dispone dell'implementazione di WinMain e CMainWindow, nonché dell'invio del menu principale. |
| STOCLIEN. Rc  | File di definizione delle risorse dell'applicazione.                                                                                        |
| STOCLIEN. Ico | Risorsa icona dell'applicazione.                                                                                                   |
| STOCLIEN. Pap | Un file di disegno cartaceo predefinito per l'applicazione.                                                                                |
| Matita. Cur   | Immagine della matita per il cursore della finestra client.                                                                                     |
| Lavandino. H       | Dichiarazione di classe per la classe dell'oggetto COM COPaperSink.                                                                      |
| Lavandino. CPP     | File di implementazione per la classe di oggetti COM COPaperSink.                                                                        |
| PAPFILE. H    | Dichiarazione di classe per la **classe CPapFile** C++.                                                                            |
| PAPFILE. CPP  | File di implementazione **per la classe CPapFile** C++.                                                                              |
| GUIPAPER. H   | Dichiarazione di classe per la **classe CGuiPaper** C++.                                                                           |
| GUIPAPER. CPP | File di implementazione **per la classe CGuiPaper** C++.                                                                             |
| STOCLIEN. Dsp | Microsoft Visual Studio Project file.                                                                                            |



 

## <a name="compound-files"></a>file compositi

**StoClien si** basa su COPaper per registrare i dati di disegno. Si basa anche su COPaper per archiviare i dati in un file composto. Tuttavia, in una tipica divisione del lavoro tra client e server COM, **StoClien** condivide parte della responsabilità dell'archiviazione file. Questa divisione del lavoro è importante nelle applicazioni COM in cui il client è un contenitore e il server è un oggetto incorporato. In questa disposizione, il client è responsabile della creazione o dell'apertura di un file di archiviazione strutturata, mentre l'oggetto server è responsabile dell'utilizzo di tale archiviazione per i propri scopi di archiviazione dei dati. Ciò può comportare la creazione di archivi secondari da parte dell'oggetto server nello spazio di archiviazione assegnato. In genere comporta la creazione di oggetti flusso nell'archiviazione da parte dell'oggetto server. L'uso dei flussi di archiviazione da parte di COPaper è descritto in dettaglio **nell'esempio StoClien.**

[**L'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) viene usata sia dall'oggetto client che dall'oggetto server per eseguire operazioni sui file. Viene usata l'implementazione di file composti dell Archiviazione strutturata. Le funzioni del servizio standard vengono usate per le operazioni su file composti. Ad esempio, la [**funzione StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) crea inizialmente un file composto e passa un puntatore **IStorage** che può essere usato per modificare il file. Questa particolare funzione viene chiamata in **StoClien.** **L'interfaccia IStorage** che ottiene viene passata come parametro a COPaper per l'uso. L'oggetto COPaper non crea o apre file composti da solo: usa le interfacce **IStorage** e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per lavorare in file composti che gli vengono dati.

Queste [**interfacce IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**e IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) non sono implementate all'interno di **StoClien** o **StoServe.** Vengono implementati all'interno delle librerie COM. Quando si ottiene un puntatore a una di queste interfacce, i relativi metodi vengono essenzialmente usati come set di servizi per operare su un file composto.

 

 




