---
title: Esempio di timeout HTTP dello scenario 1 uso della traccia ETW e dei comandi netsh
description: Tramite la traccia ETW, il flusso di dati tramite il componente API server HTTP può essere ispezionato per diagnosticare i problemi.
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa50f438aca664651b24db822f2b9e3a30da4682
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567058"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>Scenario 1: esempio di timeout HTTP con la traccia ETW e i comandi netsh

Tramite la traccia ETW, il flusso di dati tramite il componente API server HTTP può essere ispezionato per diagnosticare i problemi. Ad esempio, gli utenti di un'applicazione Web possono visualizzare messaggi di errore nel browser che non possono essere visualizzati in una pagina Web. Sul server che ospita l'applicazione Web, il professionista IT vede anche una voce di timeout della connessione all'interno del log degli errori HTTP, come illustrato nella figura 1 riportata di seguito. Il log degli errori HTTP si trova nella directory seguente:% windir% \\ system32 \\ LogFiles \\ HTTPERR \\ .

![Screenshot che mostra la finestra di comando netsh H T t P che Visualizza il log degli errori di H t T P per il timeout.](images/httperrorlog.png)

Figura 1: log degli errori HTTP per il timeout

## <a name="generating-an-etw-trace-report"></a>Generazione di un report di traccia ETW

Per generare un report di traccia ETW per il componente API server HTTP, eseguire i passaggi seguenti dal prompt dei comandi. In questo esempio, la traccia viene eseguita sul server perché ospita l'applicazione Web.

I passaggi seguenti generano una traccia denominata Httptrace. ETL, quindi convertono la traccia in un file CSV denominato httptrace.csv. Come illustrato di seguito, il provider ETW per l'API del server HTTP è denominato Microsoft-Windows-HttpService. L'opzione della riga di comando 0xFFF indica che devono essere acquisiti tutti gli eventi ETW per questo provider.

**Generare un report di traccia ETW**

1.  Avviare la traccia ETW per il componente API server HTTP: l **ogman.exe avviare Httptrace-p Microsoft-Windows-HTTPService 0xFFFF-o Httptrace. etl – ETS**
2.  Riprodurre il problema in modo che possa essere acquisito nella traccia. In questo esempio, accedere all'applicazione Web da un computer client, con la conseguente visualizzazione del messaggio "**Impossibile visualizzare la pagina**" nel client.
3.  Ora che il problema è stato riprodotto, arrestare la traccia: **logman.exe stop Httptrace – ETS**
4.  Convertire il report in formato CSV: **tracerpt.exe Httptrace. etl-of CSV-o httptrace.csv**
5.  Visualizzare il report di traccia. Di seguito è riportato un Estratto di una traccia CSV nella tabella 1.

## <a name="viewing-the-trace-and-diagnosing"></a>Visualizzazione della traccia e diagnosi

Il file CSV risultante per le tracce può essere visualizzato in Excel o in qualsiasi strumento che supporti il formato CSV. La tabella 1 seguente Mostra gli estratti da un file di traccia di esempio (httptrace.csv). Nel report di traccia la colonna "Level" Mostra una voce con un valore "3", che corrisponde a un avviso in ETW. Il componente API server HTTP segue i livelli ETW definiti nell'articolo seguente: ( https://msdn2.microsoft.com/library/aa382793.aspx) . I livelli ETW includono:



| Level | Significato      |
|-------|--------------|
| 1     | Critico     |
| 2     | Errore        |
| 3     | Avviso      |
| 4     | Infomational |
| 5     | Dettagliato      |



 

Con questo avviso, il tipo di evento (colonna di tipo) segnala "ConnTimedOut". Nelle colonne successive per l'evento ConnTimeOut, il timer specifico che è scaduto viene segnalato come "timer \_ ConnectionIdle". Si noti che la colonna con la \_ voce "timer ConnectionIdle" non è inclusa nella tabella per motivi di brevità e per evitare l'estrazione di colonne non contigue.



| Nome evento                    | Tipo            | ID evento | Versione | Channel | Level |
|-------------------------------|-----------------|----------|---------|---------|-------|
| EventTrace                    | Intestazione          | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | AddUrl          | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgReqQueueProp | 30       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect     | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn     | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq         | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Analizza           | 2        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | LogFileWrite    | 51       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnCleanup     | 24       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnTimedOut    | 53       | 0       | 16      | 3     |



 

Tabella 1: estratti da un report di traccia di esempio per un problema di timer

In questo esempio, la scadenza (evento ConnTimeOut) del timer dell'intestazione (timer \_ ConnectionIdle) è il motivo per cui gli utenti finali visualizzano il messaggio "Impossibile visualizzare la pagina" nei client Web. Un potenziale motivo del timeout potrebbe essere che i client Web stanno inviando lentamente a causa di connessioni lente. Per risolvere questo problema, è possibile modificare il valore di timeout tramite comandi netsh.

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>Regolazione del timeout tramite Netsh e verifica della soluzione

I comandi Netsh per HTTP elencati di seguito consentono a un professionista IT di visualizzare e configurare i valori delle impostazioni nel componente API del server HTTP. Le modifiche apportate ai comandi netsh HTTP hanno effetto su tutte le applicazioni Server ospitate dal componente API server HTTP per tale computer. Queste modifiche vengono mantenute tra i riavvii del componente e i riavvii del computer. I comandi netsh HTTP sono disponibili in Windows Vista e Windows Server 2008 e sostituiscono lo strumento HttpCfg.exe del Resource Kit di Windows Server 2003 durante l'esecuzione in Windows Vista e Windows Server 2008. In questo scenario si modificherà un valore di timeout e quindi si verificherà la soluzione. I timer sono disponibili nel componente API server HTTP per garantire la disponibilità e la protezione dal sovraconsumo da parte di un utente malintenzionato o configurato in modo non conforme. La regolazione dei timer dai valori predefiniti dovrebbe essere valutata attentamente rispetto a un potenziale attacco DoS.

In questo esempio, i client Web sono protetti da una connessione di rete lenta, ottenendo l' \_ evento ETW ConnectionIdle del timer. Dopo aver preso in considerazione la provocazione dei timeout e il bilanciamento dell'effetto sul carico del server, si decide di aumentare i valori di timeout a un valore di 240 secondi. È possibile visualizzare e quindi configurare il timer con la procedura riportata di seguito.

**Configurare il timer di connessione inattiva (timer \_ ConnectionIdle) con Netsh**

1.  Sul server, aprire una finestra di comando con privilegi elevati ed eseguire la procedura seguente per visualizzare e configurare il valore di timeout. Una schermata del comando netsh HTTP è illustrata nella figura 2 riportata di seguito.
2.  Mostra i valori di timeout correnti: **netsh http show timeout**
3.  Configurare il \_ valore di timeout ConnectionIdle del timer. In questo esempio il valore viene modificato in 240 secondi: **netsh http add timeout timeouttype = idleconnectiontimeout value = 240**

![finestra di comando netsh http](images/netshhttpcommand.png)

Figura 2: finestra di comando netsh HTTP

Dopo aver configurato il valore di timeout, eseguire di nuovo i passaggi di diagnostica ETW. Se la condizione di errore viene corretta, la traccia ETW non dovrebbe più visualizzare un timeout con un livello ETW "3" per il timer di inattività della connessione.

 

 




