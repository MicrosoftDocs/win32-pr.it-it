---
description: Un esperto è una libreria di collegamento dinamico (DLL) di Microsoft Win32 che analizza il traffico di rete raccolto da un provider di pacchetti di rete (NPP) e inserito in un file di acquisizione.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305944"
---
# <a name="expert"></a>Expert

Un esperto è una libreria di collegamento dinamico (DLL) di Microsoft Win32 che analizza il traffico di rete raccolto da un [*provider di pacchetti di rete*](n.md) (NPP) e inserito in un file di acquisizione. Dopo l'acquisizione e l'archiviazione dei dati in un file di acquisizione, l'esperto lavora con un parser, noto anche come parser di protocollo, per analizzare i dati nel file. Ad esempio, è possibile esaminare i frame del file di acquisizione e utilizzare un [*parser*](p.md) per riconoscere protocolli quali Server Message Block (SMB) o Transmission Control Protocol/Internet Protocol (TCP/IP).

È possibile progettare un esperto per lavorare con tutti i parser di Network Monitor e tutti i parser creati dall'utente.

Dopo che una corrispondenza richiesta di protocolli identifica un frame specifico, l'esperto estrae i dati dal frame. È possibile programmare l'esperto per manipolare le informazioni in dati utilizzabili visualizzati dal Network Monitor Visualizzatore eventi.

È possibile configurare un esperto in fase di esecuzione e quindi usare Network Monitor per salvare i dati di configurazione utente da riutilizzare con diversi file di acquisizione. È possibile utilizzare un esperto per fornire i dati di correlazione e le risoluzioni personalizzate per gli utenti finali. Per ulteriori informazioni sulla creazione di informazioni di configurazione basate su HTML, vedere la [pagina di riferimento evento](event-reference-page.md).

Durante l'installazione di Network Monitor, nella sottodirectory Experts vengono installate le dll Expert seguenti:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Quando si avvia Network Monitor, la funzione [**DllMain**](dllmain-expert.md) compila tutti gli esperti nella sottodirectory Experts. Quando l'utente seleziona **esperti** dal menu **strumenti** dell'interfaccia utente di Network Monitor, Network Monitor carica le DLL di esperti. L'esperto viene chiamato attraverso il punto di ingresso dell' [esperto di registrazione](register-expert.md) per fornire i dettagli di base sull'esperto.

![finestra di dialogo esperti di Network Monitor](images/expick.png)

Network Monitor chiama le funzioni seguenti per gestire l'esperto:

-   [**DllMain**](dllmain-expert.md)
-   [**Registra esperto**](register-expert.md)
-   [**Correre**](run.md)
-   [**Configurare**](configure.md)

L'esperto deve implementare ognuna delle funzioni precedenti.

 

 



