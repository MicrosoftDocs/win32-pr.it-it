---
title: Esempio di parser dello scenario 2 con traccia ETW
description: Per generare un report di traccia ETW per il componente API server HTTP, eseguire i passaggi illustrati in \ 0034; Generazione di un report di traccia ETW \ 0034; sezione dell'esempio di timeout HTTP dello scenario 1 usando la traccia ETW e i comandi netsh, ma riprodurre l'errore specifico di questo scenario.
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c566973b660e4e665226fbf9b4a266b086b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046756"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>Scenario 2: esempio di parser con traccia ETW

Per generare un report di traccia ETW per il componente API server HTTP, eseguire i passaggi illustrati nella sezione "generazione di un report di traccia ETW" dello [scenario 1: esempio di timeout http utilizzando la traccia ETW e i comandi netsh](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md), ma riprodurre l'errore specifico di questo scenario. In questo esempio, accedere all'applicazione Web da un computer client, ottenendo il messaggio "400 richiesta non valida" visualizzato nel client. Questi passaggi vengono eseguiti nel server perché ospita l'applicazione Web.

## <a name="viewing-the-trace-and-diagnosing"></a>Visualizzazione della traccia e diagnosi

Il file CSV risultante per le tracce può essere visualizzato in Excel o in qualsiasi strumento che supporti il formato CSV. La tabella 2 seguente Mostra gli estratti da un file di traccia di esempio (httptrace.csv). Nel report di traccia la colonna "Level" Mostra una voce con un valore "2", che rappresenta un errore. Come indicato in precedenza, il componente API server HTTP segue i livelli ETW definiti nell'articolo [tipo complesso di tipo complesso LevelType](../wes/eventmanifestschema-leveltype-complextype.md).

I livelli ETW includono: 1 critico; 2 errore; 3 avviso; 4 informazioni 5 verbose.

Con questo errore, il tipo di evento (colonna di tipo) segnala "ParseRequestFailed". Nelle colonne successive per l'evento ParseRequestFailed viene visualizzata una voce "InvalidHost". Questa voce indica che l'host identificato nella richiesta HTTP non è corretto, in base al protocollo HTTP. Si noti che la colonna con la voce "InvalidHost" non è inclusa nella tabella per motivi di brevità ed evitare l'estrazione di colonne non contigue.

Per risolvere il problema di analisi, è necessario correggere il client Web in modo che sia conforme alla specifica HTTP RFC. 

| Nome evento                    | Tipo               | ID evento | Versione | Channel | Level |
|-------------------------------|--------------------|----------|---------|---------|-------|
| EventTrace                    | Intestazione             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | AddUrl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ParseRequestFailed | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | LogFileWrite       | 51       | 0       | 16      | 4     |



 

Tabella 2: estratti da un report di traccia di esempio per un problema di analisi

 

 