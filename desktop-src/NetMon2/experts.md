---
description: Un esperto è una libreria a collegamento dinamico (DLL) Microsoft Win32 che analizza il traffico di rete raccolto da un provider di pacchetti di rete (NPP) e inserito in un file di acquisizione.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f4c3e34a9f6b8b36fdc6aa4793acfa5b652b9fa2c2117afc62943c0947af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890917"
---
# <a name="expert"></a>Expert

Un esperto è una libreria a collegamento dinamico (DLL) Microsoft Win32 che analizza il traffico di rete raccolto da un [*provider*](n.md) di pacchetti di rete (NPP) e inserito in un file di acquisizione. Dopo che i dati sono stati acquisiti e archiviati in un file di acquisizione, l'esperto lavora con un parser, detto anche parser di protocollo, per analizzare i dati nel file. Ad esempio, è possibile esaminare i frame del file di acquisizione e usare un [*parser*](p.md) per riconoscere protocolli come SMB (Server Message Block) o Transmission Control Protocol/Internet Protocol (TCP/IP).

È possibile progettare un esperto in modo che funzioni con tutti Network Monitor parser e con qualsiasi parser creato dall'utente.

Dopo che una corrispondenza richiesta di protocolli identifica un frame specifico, l'esperto estrae i dati dal frame. È possibile programmare l'esperto per modificare le informazioni in dati utilizzabili Network Monitor Visualizzatore eventi visualizzati.

È possibile configurare un esperto in fase di esecuzione e quindi usare Network Monitor per salvare i dati di configurazione utente per il riutilizzo con file di acquisizione diversi. È possibile usare un esperto per fornire dati di correlazione e risoluzioni personalizzate per gli utenti finali. Per altre informazioni sulla creazione di informazioni di configurazione basate su HTML, vedere [Pagina di riferimento eventi](event-reference-page.md).

Durante Network Monitor di installazione, nella sottodirectory Experts vengono installate le DLL degli esperti seguenti:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Quando si avvia Network Monitor, la [**funzione DllMain**](dllmain-expert.md) compila tutti gli esperti nella sottodirectory experts. Quando l'utente seleziona **Esperti** nel menu **Strumenti** dell'interfaccia Network Monitor, Network Monitor carica le DLL degli esperti. L'esperto viene chiamato tramite il punto di ingresso [Register Expert](register-expert.md) per fornire dettagli di base sull'esperto.

![Finestra di dialogo esperti di Network Monitor](images/expick.png)

Network Monitor chiama le funzioni seguenti per gestire l'esperto:

-   [**DllMain**](dllmain-expert.md)
-   [**Registrare Un esperto**](register-expert.md)
-   [**Esegui**](run.md)
-   [**Configurare**](configure.md)

L'esperto deve implementare ognuna delle funzioni precedenti.

 

 



