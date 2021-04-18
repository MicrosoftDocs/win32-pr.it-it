---
title: Creare ed eseguire l'esempio StoServe
description: Prima di poter eseguire il client, è necessario compilare l'esempio client e altri esempi correlati.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298069"
---
# <a name="create-and-run-stoserve-sample"></a>Creare ed eseguire l'esempio StoServe

Prima di poter eseguire il client, è necessario compilare l'esempio client e altri esempi correlati. Per ulteriori informazioni sulla compilazione degli esempi, vedere [How to Build Samples](how-to-build-samples.md). Se sono già stati compilati gli esempi appropriati, STOCLIEN.EXE è l'eseguibile del client da eseguire per l'esempio **StoServe** .

## <a name="code-tour"></a>Tour del codice

La tabella seguente elenca i file pertinenti per l'esempio **StoServe** .



| File        | Descrizione                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| STOSERVE.TXT | Breve descrizione di esempio                                                                                                  |
| MAKEFILE     | Il makefile generico per la compilazione dell'esempio di codice STOSERVE.DLL di questa lezione.                                            |
| STOSERVE. H   | Il file di inclusione per dichiarare come importato o definire come esportato le funzioni del servizio in STOSERVE.DLL.                 |
| STOSERVE. CPP | File di implementazione principale per STOSERVE.DLL. Dispone di DllMain e delle funzioni server COM (ad esempio, DllGetClassObject). |
| STOSERVE. DEF | Il file di definizione del modulo. Esporta le funzioni di Housing del server.                                                             |
| STOSERVE. RC  | File di definizione di risorsa DLL per l'eseguibile.                                                                      |
| STOSERVE. ICO | Risorsa icona per l'eseguibile.                                                                                     |
| Server. H     | File di inclusione per l'oggetto C++ del controllo server.                                                                       |
| Server. CPP   | Il file di implementazione per l'oggetto C++ del controllo server.                                                                |
| Fabbrica. H    | File di inclusione per gli oggetti COM class factory del server.                                                              |
| Fabbrica. CPP  | Il file di implementazione per le class factory del server.                                                                 |
| Connettersi. H    | File di inclusione per l'enumeratore del punto di connessione, il punto di connessione e le classi dell'enumeratore di connessione.                |
| Connettersi. CPP  | Il file di implementazione per l'enumeratore del punto di connessione, il punto di connessione e gli oggetti dell'enumeratore di connessione.         |
| Paper. H      | File di inclusione per la classe di oggetti COM della cocarta.                                                                        |
| Paper. CPP    | Il file di implementazione per la classe di oggetti COM della cocarta e i punti di connessione.                                       |
| STOSERVE. DSP | Microsoft Visual Studio file di progetto.                                                                                     |



 

Gli argomenti principali trattati in questa presentazione del codice sono:

-   Metodi dell'interfaccia [**iPaper**](ipaper-methods.md) .
-   Utilizzo dell'interfaccia [**IPaperSink**](ipapersink-methods.md) per le notifiche client da parte del documento.
-   [**Strutture**](structures---stoserve.md) in StoServe.
-   [Considerazioni su Unicode](unicode-considerations.md).

 

 




