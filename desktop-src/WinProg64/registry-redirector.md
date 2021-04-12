---
title: Redirector del registro di sistema
description: Il redirector del registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo viste logiche separate di determinate parti del registro di sistema in WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- Guida per programmatori Windows a 64 bit Guida alla programmazione Windows a 64 bit, redirector del registro di sistema
- Programma di reindirizzamento del registro di sistema di Windows a 64 bit
- Programmazione Windows a 64 bit per il reindirizzamento
- Programmazione Windows WOW64 a 64 bit, redirector del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c11e68f307aa014adb7cae8415f1baba155678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396175"
---
# <a name="registry-redirector"></a>Redirector del registro di sistema

Il redirector del registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo viste logiche separate di determinate parti del registro di sistema in WOW64. Il redirector del registro di sistema intercetta le chiamate al registro di sistema a 32 e 64 bit alle rispettive visualizzazioni del registro di sistema logiche e ne esegue il mapping al percorso fisico del registro di sistema corrispondente. Il processo di reindirizzamento è trasparente per l'applicazione. Pertanto, un'applicazione a 32 bit può accedere ai dati del registro di sistema come se fossero in esecuzione in Windows a 32 bit anche se i dati vengono archiviati in un percorso diverso in Windows a 64 bit.

**Windows 10 su ARM:** Oltre alla visualizzazione logica a 32 bit per le applicazioni x86, Windows 10 su ARM include una visualizzazione logica separata per le applicazioni ARM a 32 bit.

Viene condiviso un subset di chiavi in percorsi del registro di sistema reindirizzati. le chiamate al registro di sistema a 32 bit per le chiavi condivise non vengono reindirizzate. Viene invece eseguito il mapping di una copia fisica della chiave in ogni visualizzazione logica del registro di sistema. Per un elenco di chiavi reindirizzate e chiavi condivise, vedere [chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Per consentire l'interoperabilità delle applicazioni tramite COM e altri meccanismi, viene anche *riflesso* un subset di chiavi del registro di sistema reindirizzate. Il processo di reflection del registro di sistema copia le chiavi e i valori del registro di sistema tra due visualizzazioni del registro per mantenerle Sincronizza La reflection del registro di sistema è stata rimossa a partire da Windows 7 e Windows Server 2008 R2. Per altre informazioni, vedere [Reflection del registro di sistema](registry-reflection.md).

Nello scenario seguente viene illustrato l'utilizzo di queste viste logiche:

-   Un'applicazione x86 a 32 bit verifica l'esistenza della seguente chiave del registro di sistema **: \_ HKEY \_ computer locale \\ software \\ Hello**. Se la chiave non esiste, l'applicazione la crea con un valore predefinito "Hello 32-bit x86 World"; in caso contrario, legge e visualizza il valore.
-   La stessa applicazione viene modificata per scrivere "Hello 64-bit World" anziché "Hello 32-bit x86 World" e ricompilata come applicazione ARM64 o x64 a 64 bit.
-   **Windows 10 su ARM:** La stessa applicazione viene modificata per scrivere "Hello 32-bit ARM World" e ricompilata come applicazione ARM a 32 bit.
-   Quando l'applicazione x86 a 32 bit viene eseguita in Windows a 64 bit, viene visualizzato "Hello 32-bit x86 World". Quando viene eseguita l'applicazione a 64 bit, viene visualizzato "Hello 64-bit World". **Windows 10 su ARM:** Quando l'applicazione ARM a 32 bit viene eseguita su ARM64 Windows a 64 bit, Visualizza "Hello 32-bit ARM World". Tutte le applicazioni chiamano le stesse funzioni del registro di sistema con lo stesso handle predefinito e lo stesso nome di chiave. la differenza è che ogni applicazione opera sulla propria visualizzazione logica del registro di sistema e ogni visualizzazione è mappata a una posizione fisica separata del registro di sistema, in modo da mantenere intatte tutte le versioni della stringa.

Viene eseguito il mapping delle chiavi reindirizzate a percorsi fisici in **Wow6432Node**. Ad esempio, **il \_ \_ \\ software del computer locale HKEY** viene reindirizzato a **HKEY \_ \_ computer locale \\ software \\ Wow6432Node**. Tuttavia, la posizione fisica delle chiavi reindirizzate deve essere considerata riservata dal sistema. Le applicazioni non devono accedere direttamente a una posizione fisica della chiave, perché questo percorso potrebbe cambiare. Per ulteriori informazioni, vedere [accesso a una visualizzazione del registro di sistema alternativa](accessing-an-alternate-registry-view.md).

**Windows 10 su ARM:** Le chiavi del ARM a 32 bit reindirizzate sono mappate a posizioni fisiche in WowAA32Node.

Per aiutare le applicazioni a 32 bit che scrivono registri **\_ SZ** o reg, espandere i dati **\_ \_ SZ** contenenti% ProgramFiles% o% COMMONPROGRAMFILES% nel registro di sistema, WOW64 intercetta queste operazioni di scrittura e le sostituisce con "% ProgramFiles (x86)%" e "% CommonProgramFiles (x86)%". Se, ad esempio, la directory programmi si trova nell'unità C, "% ProgramFiles (x86)%" si espande in "C: \\ Program Files (x86)". La sostituzione viene eseguita solo se vengono soddisfatte le condizioni seguenti:

-   La stringa deve iniziare con% ProgramFiles% o% CommonProgramFiles%. Se la stringa inizia con uno spazio o un carattere diverso da%, non viene sostituita.
-   Il caso di% ProgramFiles% o% COMMONPROGRAMFILES% deve essere esattamente come indicato perché il confronto tra stringhe fa distinzione tra maiuscole e minuscole. Se, ad esempio, la stringa inizia con% CommonProgramFiles% anziché con% CommonProgramFiles%, non viene sostituita.
-   La stringa non può superare il \_ percorso massimo \* 2 + 15 caratteri. Se supera questa lunghezza, non viene sostituita.
-   Non è possibile aprire la chiave con la chiave \_ WOW64 \_ 64KEY. Questo flag specifica che le operazioni sulla chiave devono essere eseguite sulla visualizzazione del registro di sistema a 64 bit, quindi non vengono sostituite. Per ulteriori informazioni, vedere [accesso a una visualizzazione del registro di sistema alternativa](accessing-an-alternate-registry-view.md).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Il flag della chiave \_ WOW \_ 64 \_ 64KEY non influisce sull'eventuale sostituzione di una chiave. Questo flag influiscono sulla sostituzione a partire da Windows 7 e Windows Server 2008 R2.

Inoltre, \_ le chiavi reg SZ o reg \_ expand \_ SZ contenenti system32 vengono sostituite con SysWow64. La stringa deve iniziare con il percorso che punta a o in% windir% \\ system32. Per il confronto tra stringhe non viene fatta distinzione tra maiuscole e minuscole. Le variabili di ambiente vengono espanse prima di corrispondere al percorso, quindi vengono sostituiti tutti i percorsi seguenti:% windir% \\ system32,% SystemRoot% \\ system32 e C: \\ Windows \\ system32. Questa patch viene applicata solo alle chiavi riflesse prima di Windows 7.

Per altre informazioni, vedere i seguenti argomenti:

-   [Reflection del registro di sistema](registry-reflection.md)
-   [Chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md)
-   [Accesso a una visualizzazione del registro di sistema alternativa](accessing-an-alternate-registry-view.md)
-   [Esempio di reindirizzamento del registro di sistema in WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Accesso al registro di sistema remoto in Windows a 64 bit](remote-registry-access-in-64-bit-windows.md)

 

 




