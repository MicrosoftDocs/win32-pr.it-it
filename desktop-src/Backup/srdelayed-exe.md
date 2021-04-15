---
title: Srdelayed.exe
description: Le applicazioni che eseguono operazioni di ripristino dello stato del sistema all'avvio del sistema operativo potrebbero non essere in grado di utilizzare le funzioni di gestione file per spostare, eliminare o impostare il nome breve di determinati file di sistema.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Backup Srdelayed.exe
- Backup del ripristino dello stato del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5f6b281c07f5b0ad8d6cd7e59b4f93ec9208a5
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104474570"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Le applicazioni che eseguono operazioni di ripristino dello stato del sistema all'avvio del sistema operativo potrebbero non essere in grado di utilizzare le funzioni di gestione file per spostare, eliminare o impostare il nome breve di determinati file di sistema. Srdelayed.exe è un file eseguibile, fornito con la funzionalità Windows Server Backup (WSB) in Windows Server 2008, che consente alle applicazioni di ripristino dello stato del sistema di spostare, eliminare e impostare il nome breve dei file di sistema.

Lo strumento Srdelayed è destinato alle applicazioni di ripristino dello stato del sistema; non sostituisce le funzioni di gestione file. Questo strumento deve essere utilizzato solo quando l'applicazione non è in grado di spostare, eliminare o impostare il nome breve di un file di sistema utilizzando le funzioni [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa), [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)e [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) . Durante il ripristino e il riavvio dello stato del sistema, Srdelayed.exe viene utilizzato da ripristino configurazione di sistema e dallo strumento da riga di comando wbadmin.exe per spostare, eliminare e impostare il nome breve in alcuni file di sistema. Srdelayed può quindi essere utile per gli sviluppatori che richiedono la possibilità di ripristinare questi file di sistema nelle proprie applicazioni di ripristino dello stato del sistema.

Srdelayed può eseguire le operazioni seguenti:

-   Operazione di spostamento del file simile alla funzione [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con **ritardo MOVEFILE \_ \_ fino al \_** flag di riavvio
-   Operazione Delete file simile alla funzione [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Operazione di impostazione del nome breve simile alla funzione [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Per usare Srdelayed, l'applicazione richiede il percorso completo del file di Srdelayed.exe e il percorso completo di un file di testo Unicode che è stato creato per contenere le informazioni necessarie allo strumento per eseguire tutte le operazioni di gestione dei file richieste. L'applicazione è responsabile di garantire che il file di testo non contenga richieste ridondanti per un'operazione e che gestisca l'ordine richiesto delle operazioni di gestione file. Ad esempio, poiché una cartella deve essere vuota per essere eliminata, l'applicazione deve garantire che il file di testo specifichi la rimozione di tutti i file all'interno della cartella prima di richiedere l'eliminazione della cartella.

Se la voce **SetupExecute** non esiste già nel registro di sistema, l'applicazione deve creare una voce di tipo **reg \_ \_ multisz** denominata **SetupExecute** nella seguente chiave del registro di sistema: **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

L'applicazione deve usare il formato seguente per impostare il valore di **SetupExecute** sul percorso completo della posizione del file di Srdelayed.exe e il percorso completo della posizione del file di testo. Anteporre " \\ \\ ?? \\ " al percorso del file di testo, come indicato di seguito:

*Percorso completo per Srdelayed.exe* \\ ? \\ \\ *Percorso completo del file di testo*  


Ad esempio, il valore seguente per **SetupExecute** indica che il Srdelayed.exe si trova nella cartella system32 e il file di testo è denominato DelayedOperations:

C: \\ Windows \\ system32 \\srdelayed.exe \\ \\ ? \\ C: \\ temp \\ DelayedOperations  


Gli spazi nel percorso e nel nome devono essere codificati in formato esadecimale. Per *i file di programma*, ad esempio, codificare il percorso come " \\ \\ ?? \\ C:Program%20Files \\a.dll ".

Quando il registro di sistema o il sistema viene ripristinato al riavvio, l'applicazione deve assicurarsi che **SetupExecute** venga scritto nell'hive del registro di sistema corretto. Il ripristino del registro di sistema viene eseguito prima dell'esecuzione Srdelayed.exe. L'applicazione deve scrivere **SetupExecute** nella versione ripristinata del registro di sistema, perché si tratta della versione che viene letta.

## <a name="format-for-the-srdelayed-input-file"></a>Formato per il file di input Srdelayed

Tutte le informazioni Srdelayed devono eseguire operazioni di gestione dei file sono specificate come una stringa di caratteri Unicode in un file di testo Unicode. La stringa di caratteri Unicode viene partizionata in record ognuno dei quali è partizionato in quattro campi. Ogni record specifica un singolo file di spostamento, un file di eliminazione o l'operazione di impostazione del nome breve. I quattro campi di ogni record contengono i parametri per l'operazione. Srdelayed.exe esegue ogni operazione nell'ordine in cui si verificano i record nella stringa. L'applicazione deve verificare la presenza di eventuali record duplicati in questo file e rimuovere i duplicati.

Nella stringa seguente viene illustrato il formato di un file che richiede due operazioni e costituito da due record. Ogni campo di parametro termina con un singolo carattere L' \\ 0'. Un record è costituito da quattro campi consecutivi. \\Alla fine di tutti i record viene aggiunto un carattere aggiuntivo a L'0'.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


Il significato dei campi primo, secondo, terzo e quarto parametro varia a seconda che il record Descriva un'operazione di spostamento, eliminazione o impostazione del nome breve.

## <a name="format-for-a-move-file-record"></a>Formato per un record del file di spostamento

Il campo 1 lo identifica come una richiesta di spostamento di un file. Il valore in questo campo è sempre L "MoveFile" e fa distinzione tra maiuscole e minuscole.

Il campo 2 specifica il percorso di origine del file. L'operazione di spostamento del file Srdelayed non supporta lo spostamento di una cartella. È necessario specificare un file in questo campo. Il valore di questo campo è il percorso completo del file accodato a " \\ \\ ?? \\ ", a meno che il percorso non includa un identificatore univoco globale (Guid), che usa " \\ \\ ? \\ " come prefisso. Rimuovere " \\ \\ ? \\ " prima di aggiungere a " \\ \\ ?? \\ ".

Il campo 3 specifica la destinazione del file. L'operazione di spostamento del file funziona solo all'interno di un volume. L'origine e la destinazione devono trovarsi nello stesso volume. Il valore di questo campo è il percorso completo del file accodato a " \\ \\ ?? \\ ", a meno che il percorso non includa un identificatore univoco globale (Guid), che usa " \\ \\ ? \\ " come prefisso. Rimuovere " \\ \\ ? \\ " prima di aggiungere a " \\ \\ ?? \\ ".

Il campo 4 riceve informazioni sullo stato da Srdelayed. Il valore in questo campo deve essere impostato su L "NotExecuted" per un nuovo record.

Nell'esempio seguente viene fatto riferimento al file in base al percorso dell'unità. Se il percorso e il nome dell'origine sono C: \\ Stage \\a.dll, questo record richiede che Srdelayed lo sposti in c: \\ temp \\a.dll.

MoveFile \\ \\ ? \\ C: \\ \\a.dll temporanea \\ \\ ? \\ C: \\ temp \\a.dll NotExecuted  


Nell'esempio seguente viene fatto riferimento al file in base al percorso GUID del volume. Se il percorso e il nome dell'origine sono \\ \\ ? \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ fase \\a.dll, questo record richiede che Srdelayed lo sposti \\ \\ ? \\a.dll Temp del volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ \\

 MoveFile \\ \\ ? \\a.dll fase del volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ \\ \\ \\ ? \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Formato per un record di file Delete

Il campo 1 lo identifica come una richiesta di eliminazione di un file. Il valore in questo campo è sempre L "DeleteFile" e fa distinzione tra maiuscole e minuscole.

Il campo 2 non è usato. Il valore in questo campo deve essere impostato su L "inutilizzato".

Il campo 3 specifica il file da rimuovere. Per rimuovere una cartella, è necessario che sia vuota. Utilizzare le operazioni di eliminazione file per rimuovere tutti i file nella cartella prima di rimuovere la cartella. Il valore di questo campo è il percorso completo del file accodato a " \\ \\ ?? \\ ", a meno che il percorso non includa un identificatore univoco globale (Guid), che usa " \\ \\ ? \\ " come prefisso. Rimuovere " \\ \\ ? \\ " prima di aggiungere a " \\ \\ ?? \\ ".

Il campo 4 riceve informazioni sullo stato da Srdelayed. Il valore in questo campo deve essere impostato su L "NotExecuted" per un nuovo record.

Nell'esempio seguente viene fatto riferimento al file in base al percorso dell'unità. Se il percorso e il nome sono C: \\ temp \\b.dll, questo record richiede che Srdelayed elimini il file.

DeleteFile non usato \\ \\ ? \\ C: \\ temp \\b.dll NotExecuted  


Nell'esempio seguente viene fatto riferimento al file in base al GUID del volume. Se il percorso e il nome sono \\ \\ ? \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ temp \\b.dll, questo record richiede che Srdelayed rimuova il file.

DeleteFile non usato \\ \\ ? \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Formato per il record di set Short-Name

Il campo 1 lo identifica come una richiesta di impostazione del nome breve di un file. Il valore in questo campo è sempre L "SetFileShortName" e fa distinzione tra maiuscole e minuscole.

Il campo 2 specifica il nome breve.

Campo 3 specifica il percorso e il nome lungo per la ricezione del nome breve. Il valore di questo campo è il percorso e il nome lungo del file accodato a " \\ \\ ?? \\ ", a meno che il percorso non includa un identificatore univoco globale (Guid), che usa " \\ \\ ? \\ " come prefisso. Rimuovere " \\ \\ ? \\ " prima di aggiungere a " \\ \\ ?? \\ ".

Il campo 4 riceve informazioni sullo stato da Srdelayed. Il valore in questo campo deve essere impostato su L "NotExecuted" per un nuovo record.

Nell'esempio seguente viene fatto riferimento al file in base al percorso dell'unità. Se il percorso e il nome del file sono C: \\ temp \\ShortFileName.dll, questo record richiede che il file riceva un nome breve, shortn ~1.dll.

SetFileShortName shortn ~1.dll \\ \\ ? \\ C: \\ temp \\ShortFileName.dll NotExecuted  


Nell'esempio seguente viene fatto riferimento al file in base al GUID del volume. Se il percorso e il nome del file sono \\ \\ \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ , questo record richiede che il file riceva un nome breve, shortn ~1.dll.

SetFileShortName shortn ~1.dll \\ \\ ? \\ Volume {26a21bda-a627-11D7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Stato delle operazioni di Srdelayed

Srdelayed scrive la stringa L "SC =*xxxxxxx*" nel quarto campo di ogni record del file di testo, dove *xxxxxxx* è un valore esadecimale che indica lo stato dell'operazione richiesta. Un valore pari a zero indica che l'operazione è riuscita.

Srdelayed crea una chiave del registro di sistema denominata **SystemRestore** in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** per registrare il risultato dell'intera operazione di ripristino. Se Srdelayed esegue tutte le operazioni richieste con esito positivo, il nome RestoreStatusResult viene scritto sotto questa chiave con un valore zero. Se Srdelayed non è in grado di eseguire alcuna delle operazioni richieste, i nomi RestoreStatusResult e RestoreStatusDetails vengono scritti sotto questa chiave con valori diversi da zero. Il nome RestoreStatusDetails viene scritto in base a questa chiave solo se Srdelayed non è in grado di eseguire le operazioni richieste. Se un'operazione per impostare il nome breve di un file ha esito negativo, Srdelayed continua con l'operazione successiva. Srdelayed considera cruciali le operazioni di spostamento del file e di eliminazione dei file e non continua se un'operazione di spostamento o eliminazione ha esito negativo.

 

 