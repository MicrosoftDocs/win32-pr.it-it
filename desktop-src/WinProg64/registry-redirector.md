---
title: Redirector del Registro di sistema
description: Il redirector del Registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo visualizzazioni logiche separate di determinate parti del Registro di sistema in WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- Guida alla programmazione a 64 bit Windows programmazione a 64 bit Windows programmazione di , redirector del Registro di sistema
- redirector del Registro di sistema a 64 bit Windows programmazione
- reindirizzamento della programmazione Windows a 64 bit
- WOW64 a 64 bit Windows programmazione , redirector del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac810a6ce2dba049f7b7e5b9d28386cda89712f2833eb7bf4f7892df59b34ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561507"
---
# <a name="registry-redirector"></a>Redirector del Registro di sistema

Il redirector del Registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo visualizzazioni logiche separate di determinate parti del Registro di sistema in WOW64. Il redirector del Registro di sistema intercetta le chiamate del Registro di sistema a 32 bit e a 64 bit alle rispettive viste logiche del Registro di sistema ed esegue il mapping al percorso fisico corrispondente del Registro di sistema. Il processo di reindirizzamento è trasparente per l'applicazione. Pertanto, un'applicazione a 32 bit può accedere ai dati del Registro di sistema come se fosse in esecuzione in un Windows a 32 bit anche se i dati vengono archiviati in un percorso diverso in un Windows a 64 bit.

**Windows 10 in ARM:** Oltre alla visualizzazione logica a 32 bit per le applicazioni x86, Windows 10 in ARM include una visualizzazione logica separata per le applicazioni ARM a 32 bit.

Viene condiviso un subset di chiavi nei percorsi del Registro di sistema reindirizzati. Le chiamate del Registro di sistema a 32 bit alle chiavi condivise non vengono reindirizzate. Viene invece eseguito il mapping di una copia fisica della chiave in ogni vista logica del Registro di sistema. Per un elenco di chiavi reindirizzate e chiavi condivise, vedere Chiavi [del Registro di sistema interessate da WOW64.](shared-registry-keys.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Per abilitare l'interoperabilità delle applicazioni tramite COM e altri meccanismi, viene riflessa anche un subset di chiavi del Registro di sistema *reindirizzate.* Il processo di reflection del Registro di sistema copia le chiavi e i valori del Registro di sistema tra due viste del Registro di sistema per mantenerle sincronizzate. La reflection del Registro di sistema è stata rimossa a partire da Windows 7 e Windows Server 2008 R2. Per altre informazioni, vedere Reflection [del Registro di sistema.](registry-reflection.md)

Lo scenario seguente illustra l'uso di queste viste logiche:

-   Un'applicazione x86 a 32 bit verifica l'esistenza della chiave del Registro di sistema seguente: **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Hello**. Se la chiave non esiste, l'applicazione la crea con il valore predefinito "Hello 32-bit x86 world"; In caso contrario, legge e visualizza il valore.
-   La stessa applicazione viene modificata per scrivere "Hello world a 64 bit" anziché "Hello 32-bit x86 world" e ricompilata come applicazione x64 o ARM64 a 64 bit.
-   **Windows 10 in ARM:** La stessa applicazione viene modificata per scrivere "Hello 32-bit ARM world" e ricompilata come applicazione ARM a 32 bit.
-   Quando l'applicazione x86 a 32 bit viene eseguita in un Windows a 64 bit, viene visualizzato "Hello 32-bit x86 world". Quando viene eseguita l'applicazione a 64 bit, viene visualizzato "Hello world a 64 bit". **Windows 10 in ARM:** Quando l'applicazione ARM a 32 bit viene eseguita in arm64 Windows a 64 bit, viene visualizzato "Hello 32-bit ARM world". Tutte le applicazioni chiamano le stesse funzioni del Registro di sistema con lo stesso handle predefinito e lo stesso nome di chiave; La differenza è che ogni applicazione opera sulla visualizzazione logica del Registro di sistema e ogni vista viene mappata a una posizione fisica separata del Registro di sistema, mantenendo intatte tutte le versioni della stringa.

Le chiavi reindirizzate vengono mappate a posizioni fisiche in **Wow6432Node.** Ad esempio, **HKEY \_ LOCAL MACHINE \_ \\ Software** viene reindirizzato a **HKEY LOCAL MACHINE Software \_ \_ \\ \\ Wow6432Node**. Tuttavia, la posizione fisica delle chiavi reindirizzate deve essere considerata riservata dal sistema. Le applicazioni non devono accedere direttamente alla posizione fisica di una chiave, perché questa posizione può cambiare. Per altre informazioni, vedere [Accesso a una visualizzazione alternativa del Registro di sistema.](accessing-an-alternate-registry-view.md)

**Windows 10 in ARM:** Le chiavi ARM a 32 bit reindirizzate vengono mappate a posizioni fisiche in WowAA32Node.

Per consentire alle applicazioni a 32 bit che scrivono dati **REG \_ SZ** o **REG EXPAND \_ \_ SZ** contenenti %ProgramFiles% o %commonprogramfiles% nel Registro di sistema, WOW64 intercetta queste operazioni di scrittura e le sostituisce con "%ProgramFiles(x86)%" e "%commonprogramfiles(x86)%". Ad esempio, se la directory Programmi si trova nell'unità C, "%ProgramFiles(x86)%" si espande in "C: \\ Programmi (x86)". La sostituzione viene eseguita solo se vengono soddisfatte le condizioni seguenti:

-   La stringa deve iniziare con %ProgramFiles% o %commonprogramfiles%. Se la stringa inizia con uno spazio o un carattere diverso da %, non viene sostituita.
-   La distinzione tra maiuscole e minuscole di %ProgramFiles% o %commonprogramfiles% deve essere esattamente come illustrato perché il confronto tra stringhe fa distinzione tra maiuscole e minuscole. Ad esempio, se la stringa inizia con %CommonProgramFiles% anziché con %commonprogramfiles%, non viene sostituita.
-   La stringa non può superare i \_ \* 2+15 caratteri max PATH. Se supera questa lunghezza, non viene sostituito.
-   La chiave non può essere aperta con KEY \_ WOW64 \_ 64KEY. Questo flag specifica che le operazioni sulla chiave devono essere eseguite nella vista del Registro di sistema a 64 bit, quindi non viene sostituita. Per altre informazioni, vedere [Accesso a una visualizzazione alternativa del Registro di sistema.](accessing-an-alternate-registry-view.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Il flag KEY \_ WOW \_ 64 \_ 64KEY non influisce sulla sostituzione di una chiave. Questo flag influisce sulla sostituzione a partire da Windows 7 e Windows Server 2008 R2.

Inoltre, le chiavi REG SZ o REG EXPAND SZ contenenti \_ \_ \_ system32 vengono sostituite con syswow64. La stringa deve iniziare con il percorso che punta a o in %windir% \\ system32. Il confronto tra stringhe non fa distinzione tra maiuscole e minuscole. Le variabili di ambiente vengono espanse prima di trovare la corrispondenza con il percorso, quindi vengono sostituiti tutti i percorsi seguenti: %windir% \\ system32, %SystemRoot% \\ system32 e C: \\ windows \\ system32. Questa patch viene applicata solo alle chiavi riflesse prima Windows 7.

Per altre informazioni, vedere i seguenti argomenti:

-   [Reflection del Registro di sistema](registry-reflection.md)
-   [Chiavi del Registro di sistema interessate da WOW64](shared-registry-keys.md)
-   [Accesso a una visualizzazione alternativa del Registro di sistema](accessing-an-alternate-registry-view.md)
-   [Esempio di reindirizzamento del Registro di sistema in WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Accesso al Registro di sistema remoto in Windows](remote-registry-access-in-64-bit-windows.md)

 

 




