---
title: Srdelayed.exe
description: Le applicazioni che eseguono operazioni di ripristino dello stato del sistema all'inizio dell'avvio del sistema operativo potrebbero non essere in grado di usare le funzioni di gestione file per spostare, eliminare o impostare il nome breve di determinati file di sistema.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe backup
- Backup del ripristino dello stato del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdf95ff77fd17a578b85e6037c71146666eae9522d066bc1c4629fb9a2c24e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835539"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Le applicazioni che eseguono operazioni di ripristino dello stato del sistema all'inizio dell'avvio del sistema operativo potrebbero non essere in grado di usare le funzioni di gestione file per spostare, eliminare o impostare il nome breve di determinati file di sistema. Srdelayed.exe è un file eseguibile, fornito con la funzionalità Windows Server Backup (WSB) in Windows Server 2008, che consente alle applicazioni di ripristino dello stato del sistema di spostare, eliminare e impostare il nome breve dei file di sistema.

Lo strumento Srdelayed è destinato alle applicazioni di ripristino dello stato del sistema. non sostituisce le funzioni di gestione file. Questo strumento deve essere usato solo quando l'applicazione non è in grado di spostare, eliminare o impostare il nome breve di un file di sistema usando le funzioni [**MoveFileEx,**](/windows/desktop/api/winbase/nf-winbase-movefileexa) [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)e [**SetFileShortName.**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) Durante un ripristino e un riavvio dello stato del sistema, Srdelayed.exe viene usato da Ripristino configurazione di sistema e dallo strumento da riga di comando wbadmin.exe per spostare, eliminare e impostare il nome breve in determinati file di sistema. Srdelayed può quindi essere utile per gli sviluppatori che richiedono la possibilità di ripristinare questi file di sistema nelle proprie applicazioni di ripristino dello stato del sistema.

Srdelayed può eseguire le operazioni seguenti:

-   Operazione di spostamento del file simile alla [**funzione MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con il flag **MOVEFILE \_ DELAY UNTIL \_ \_ REBOOT**
-   Operazione di eliminazione file simile alla [**funzione DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Operazione di impostazione del nome breve simile alla [**funzione SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Per usare Srdelayed, l'applicazione richiede il percorso completo del file Srdelayed.exe e il percorso completo di un file di testo Unicode creato per contenere le informazioni necessarie per eseguire tutte le operazioni di gestione file richieste. L'applicazione è responsabile di garantire che questo file di testo non contenga richieste ridondanti per un'operazione e che gestisca qualsiasi ordinamento necessario delle operazioni di gestione dei file. Ad esempio, poiché una cartella deve essere vuota per essere eliminata, l'applicazione deve assicurarsi che il file di testo specifichi la rimozione di tutti i file all'interno della cartella prima di richiedere l'eliminazione della cartella.

Se la voce **SetupExecute** non esiste già nel Registro di sistema, l'applicazione deve creare una voce di tipo **REG MULTI \_ \_ SZ** denominata **SetupExecute** nella chiave del Registro di sistema **seguente: HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

L'applicazione deve usare il formato seguente per impostare il valore di **SetupExecute** sul percorso completo del file Srdelayed.exe e il percorso completo del file di testo. Aggiungere il \\ \\ prefisso " ?? \\ " al percorso del file di testo, come indicato di seguito:

*Full Path to Srdelayed.exe* \\ \\ ?? \\ *Percorso completo del file di testo*  


Ad esempio, il valore seguente per **SetupExecute** indica che il Srdelayed.exe si trova nella cartella System32 e che il file di testo è denominato DelayedOperations:

C: \\ Windows \\ System32 \\srdelayed.exe \\ \\ ?? \\ C: \\ temp \\ DelayedOperations  


Gli spazi nel percorso e nel nome devono essere con codifica esadecimale. Ad esempio, per *Programmi*, codificare il percorso come " \\ \\ ?? \\ C:Program%20Files \\a.dll".

Quando il Registro di sistema o il sistema viene ripristinato al riavvio, l'applicazione deve assicurarsi che **SetupExecute** venga scritto nell'hive del Registro di sistema corretto. Il ripristino del Registro di sistema viene eseguito prima Srdelayed.exe'esecuzione. L'applicazione deve **scrivere SetupExecute** nella versione ripristinata del Registro di sistema perché si tratta della versione letta.

## <a name="format-for-the-srdelayed-input-file"></a>Formato per il file di input srdelayed

Tutte le informazioni necessarie a Srdelayed per eseguire operazioni di gestione dei file vengono specificate come stringa di caratteri Unicode in un file di testo Unicode. La stringa di caratteri Unicode viene partizionata in record che sono a loro volta partizionati in quattro campi. Ogni record specifica un singolo file di spostamento, un file di eliminazione o un'operazione di impostazione del nome breve. I quattro campi di ogni record contengono i parametri per l'operazione. Srdelayed.exe esegue ogni operazione nell'ordine in cui i relativi record si verificano nella stringa. L'applicazione deve verificare la presenza di eventuali record duplicati in questo file e rimuovere i duplicati.

La stringa seguente illustra il formato di un file che richiede due operazioni ed è costituito da due record. Ogni campo di parametro termina con un singolo carattere L' \\ 0'. Un record è costituito da quattro campi consecutivi. Un carattere L' \\ 0' aggiuntivo viene aggiunto alla fine di tutti i record.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


Il significato del primo, del secondo, del terzo e del quarto campo di parametro dipende dal fatto che il record descriva un'operazione di spostamento, eliminazione o impostazione del nome breve.

## <a name="format-for-a-move-file-record"></a>Formato per un record di spostamento file

Il campo 1 lo identifica come una richiesta di spostamento di un file. Il valore in questo campo è sempre L"MoveFile" e fa distinzione tra maiuscole e minuscole.

Il campo 2 specifica il percorso di origine del file. L'operazione Srdelayed move file non supporta lo spostamento di una cartella. In questo campo è necessario specificare un file. Il valore per questo campo è il percorso completo del file aggiunto a " ?? " a meno che il percorso non includa un identificatore univoco globale (GUID), che usa \\ \\ " ? " \\ come \\ \\ \\ prefisso. Rimuovere " \\ \\ ? " prima di aggiungere a \\ " \\ \\ ?? \\ ".

Il campo 3 specifica la destinazione del file. L'operazione di spostamento del file funziona solo all'interno di un volume. L'origine e la destinazione devono essere nello stesso volume. Il valore per questo campo è il percorso completo del file aggiunto a " ?? " a meno che il percorso non includa un identificatore univoco globale (GUID), che usa \\ \\ " ? " \\ come \\ \\ \\ prefisso. Rimuovere " \\ \\ ? " prima di aggiungere a \\ " \\ \\ ?? \\ ".

Il campo 4 riceve informazioni sullo stato da Srdelayed. Il valore in questo campo deve essere impostato su L"NotExecuted" per un nuovo record.

Nell'esempio seguente viene fatto riferimento al file in base al percorso dell'unità. Se il percorso e il nome dell'origine sono C: Stagea.dll, questo record richiede che Srdelayed lo sposti \\ \\ in C: temp \\ \\a.dll.

MoveFile \\ \\ ?? \\ C: \\ Stage \\a.dll \\ \\ ?? \\ C: \\ temp \\a.dll NotExecuted  


L'esempio seguente fa riferimento al file in base al percorso GUID del volume. Se il percorso e il nome dell'origine sono \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} Stagea.dll, questo record richiede che \\ \\ Srdelayed lo sposti in \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll

 MoveFile \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ Stage \\a.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Formato per un record di file di eliminazione

Il campo 1 lo identifica come una richiesta di eliminazione di un file. Il valore in questo campo è sempre L"DeleteFile" e fa distinzione tra maiuscole e minuscole.

Il campo 2 non è usato. Il valore in questo campo deve essere impostato su L"Unused".

Il campo 3 specifica il file da rimuovere. Una cartella deve essere vuota per essere rimossa. Usare le operazioni di eliminazione file per rimuovere tutti i file nella cartella prima di rimuovere la cartella. Il valore per questo campo è il percorso completo del file aggiunto a " ?? " a meno che il percorso non includa un identificatore univoco globale (GUID), che usa \\ \\ " ? " \\ come \\ \\ \\ prefisso. Rimuovere " \\ \\ ? " prima di aggiungere a \\ " \\ \\ ?? \\ ".

Il campo 4 riceve informazioni sullo stato da Srdelayed. Il valore in questo campo deve essere impostato su L"NotExecuted" per un nuovo record.

Nell'esempio seguente viene fatto riferimento al file in base al percorso dell'unità. Se il percorso e il nome sono C: tempb.dll, questo record richiede \\ \\ a Srdelayed di eliminare il file.

DeleteFile Unused \\ \\ ?? \\ C: \\ temp \\b.dll NotExecuted  


L'esempio seguente fa riferimento al file in base al GUID del volume. Se il percorso e il nome sono \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963}b.dll temp, questo record richiede a \\ \\ Srdelayed di rimuovere il file.

DeleteFile Unused \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Formato per Set Short-Name Record

Il campo 1 lo identifica come una richiesta per impostare il nome breve di un file. Il valore in questo campo è sempre L"SetFileShortName" e fa distinzione tra maiuscole e minuscole.

Il campo 2 specifica il nome breve.

Il campo 3 specifica il percorso e il nome lungo per ricevere il nome breve. Il valore per questo campo è il percorso e il nome lungo del file aggiunto a " ?? " a meno che il percorso non includa un identificatore univoco globale (GUID), che usa " ? " come \\ \\ \\ \\ \\ \\ prefisso. Rimuovere " \\ \\ ? " prima di aggiungere a \\ " \\ \\ ?? \\ ".

Il campo 4 riceve informazioni sullo stato da Srdelayed. Il valore in questo campo deve essere impostato su L"NotExecuted" per un nuovo record.

Nell'esempio seguente viene fatto riferimento al file in base al percorso dell'unità. Se il percorso e il nome del file sono C: tempShortFileName.dll, questo record richiede che il file riceva un nome \\ \\ breve, ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ C: \\ temp \\ShortFileName.dll NotExecuted  


L'esempio seguente fa riferimento al file in base al GUID del volume. Se il percorso e il nome del file è \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963}ShortFileName.dlltemp , questo record richiede che il file riceva un nome \\ \\ \\ breve, ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Stato delle operazioni srdelayed

Srdelayed scrive la stringa L"SC=*xxxxxxx*" nel quarto campo di ogni record del file di testo, dove *xxxxxxx è* un valore esadecimale che indica lo stato dell'operazione richiesta. Il valore zero indica che l'operazione è riuscita.

Srdelayed crea una chiave del Registro di sistema denominata **SystemRestore** in **HKEY \_ LOCAL \_ MACHINE** Software Microsoft Windows NT CurrentVersion per registrare il risultato \\  \\  \\  \\  dell'intera operazione di ripristino. Se Srdelayed esegue tutte le operazioni richieste con esito positivo, il nome RestoreStatusResult viene scritto in questa chiave con un valore zero. Se Srdelayed non è in grado di eseguire nessuna delle operazioni richieste, i nomi RestoreStatusResult e RestoreStatusDetails vengono scritti in questa chiave con valori diversi da zero. Il nome RestoreStatusDetails viene scritto in questa chiave solo se Srdelayed non è in grado di eseguire le operazioni richieste. Se un'operazione per impostare il nome breve di un file non riesce, Srdelayed continua con l'operazione successiva. Srdelayed considera critiche le operazioni di spostamento ed eliminazione del file e non continua se un'operazione di spostamento o eliminazione non riesce.

 

 