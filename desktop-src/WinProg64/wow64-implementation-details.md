---
title: Dettagli di implementazione di WOW64
description: L'emulatore WOW64 viene eseguito in modalità utente.
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- Programmazione Windows WOW64 a 64 bit, variabili di ambiente
- Programmazione Windows WOW64 a 64 bit, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117938"
---
# <a name="wow64-implementation-details"></a>Dettagli di implementazione di WOW64

L'emulatore WOW64 viene eseguito in modalità utente. Fornisce un'interfaccia tra la versione a 32 bit di Ntdll.dll e il kernel del processore e intercetta le chiamate al kernel. L'emulatore WOW64 è costituito dalle DLL seguenti:

-   Wow64.dll fornisce l'infrastruttura di emulazione principale e i thunk per le funzioni del punto di ingresso Ntoskrnl.exe.
-   Wow64Win.dll fornisce i thunk per le funzioni del punto di ingresso Win32k.sys.
-   (solo x64) Wow64Cpu.dll fornisce supporto per l'esecuzione di programmi x86 in x64.
-   (Solo Intel Itanium) IA32Exec. bin contiene l'emulatore software x86.
-   (Solo Intel Itanium) Wowia32x.dll fornisce l'interfaccia tra IA32Exec. bin e WOW64.
-   (Solo ARM64) xtajit.dll contiene l'emulatore software x86.
-   (Solo ARM64) wowarmw.dll fornisce supporto per l'esecuzione di programmi ARM32 in ARM64.

Queste dll, insieme alla versione a 64 bit di Ntdll.dll, sono gli unici file binari a 64 bit che possono essere caricati in un processo a 32 bit. In Windows 10 su ARM, i file binari di CHPE (compilati Hybrid Portable Executable) possono essere caricati anche in un processo x86 a 32 bit.

All'avvio Wow64.dll carica la versione x86 di Ntdll.dll (o la versione CHPE, se abilitata) ed esegue il codice di inizializzazione, che carica tutte le dll a 32 bit necessarie. Quasi tutte le dll a 32 bit sono copie non modificate dei file binari di Windows a 32 bit, anche se alcune sono caricate come CHPE per motivi di prestazioni. Alcune di queste dll si comportano in modo diverso in WOW64 rispetto a quelle eseguite su Windows a 32 bit, in genere perché condividono memoria con componenti di sistema a 64 bit. Tutto lo spazio degli indirizzi in modalità utente superiore al limite di 32 bit è riservato dal sistema. Per altre informazioni, vedere [utilizzo delle prestazioni e della memoria in WOW64](performance-and-memory-consumption.md).

Anziché utilizzare la sequenza di chiamate del servizio di sistema x86, i file binari a 32 bit che eseguono chiamate di sistema vengono ricompilati per l'utilizzo di una sequenza chiamante personalizzata. Questa sequenza di chiamata è conveniente per l'intercettazione di WOW64 perché rimane interamente in modalità utente. Quando viene rilevata la sequenza di chiamata personalizzata, la CPU WOW64 esegue la transizione alla modalità nativa a 64 bit e chiama Wow64.dll. Il thunk viene eseguito in modalità utente per ridurre l'effetto sul kernel a 64 bit e per ridurre il rischio di un bug nel thunk che può causare un arresto anomalo della modalità kernel, il danneggiamento dei dati o un problema di sicurezza. I thunk estraggono gli argomenti dallo stack a 32 bit, li estendono a 64 bit, quindi effettuano la chiamata al sistema nativo.

## <a name="environment-variables"></a>Variabili di ambiente

Quando un processo a 32 bit viene creato da un processo a 64 bit o quando un processo a 64 bit viene creato da un processo a 32 bit, WOW64 imposta le variabili di ambiente per il processo creato, come illustrato nella tabella seguente.



| Processo                   | Variabili di ambiente                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| processo a 64 bit<br/> | Architettura del processore \_ = amd64 o \_ architettura del processore = IA64 o architettura del processore \_ = arm64<br/> ProgramFiles =% ProgramFiles%<br/> ProgramW6432 =% programmi%<br/> CommonProgramFiles =% CommonProgramFiles%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Le variabili di ambiente ProgramW6432 e CommonProgramW6432 sono state aggiunte a partire da Windows 7 e Windows Server 2008 R2. <br/> |
| processo a 32 bit<br/> | Architettura del processore \_ = x86<br/> \_ARCHITEW6432 processore =% \_ Architettura processore%<br/> ProgramFiles =% ProgramFiles (x86)%<br/> ProgramW6432 =% programmi%<br/> CommonProgramFiles =% CommonProgramFiles (x86)%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>Hook globali

La funzione [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) può essere usata per inserire una dll in un altro processo se vengono soddisfatte le condizioni seguenti:

-   Una DLL a 32 bit può essere inserita solo in un processo a 32 bit ed è possibile inserire una DLL a 64 bit solo in un processo a 64 bit. Non è possibile inserire una DLL a 32 bit in un processo a 64 bit o viceversa.
-   Le dll a 32 bit e a 64 bit devono avere nomi diversi.
-   Le architetture della DLL e del processo devono corrispondere. Ad esempio, non è possibile inserire una DLL x86 a 32 bit in un processo ARM a 32 bit.

Per ulteriori informazioni, vedere [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).

Tenere presente che il **\_ mouse WH**, **la \_ tastiera WH**, il **\_ \* Journal** di WH, la **\_ Shell di WH** e gli hook di basso livello possono essere chiamati sul thread che ha installato l'hook anziché sul thread che elabora l'hook. Per questi hook, è possibile che vengano chiamati entrambi i Hook a 32 bit e a 64 bit se un hook a 32 bit precede un hook a 64 bit nella catena di hook. Per ulteriori informazioni, vedere [utilizzo degli hook](../winmsg/using-hooks.md).

 

