---
title: Esecuzione di applicazioni a 32 bit
description: Eseguire facilmente applicazioni Windows a 32 bit su Windows a 64 bit con l'emulatore WOW64 x86. Informazioni anche sul director del Registro di sistema, file system redirector, sull'installazione dell'applicazione in sistemi a 64 bit e sul debug di WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- Programmazione Windows WOW64 a 64 bit
- Wow64 a 64 bit Windows programmazione , informazioni su
- Applicazioni a 32 bit in applicazioni Windows a 64 bit Windows programmazione
- Guida alla programmazione Windows a 64 bit Windows , WOW64 Vedere WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1da192f4109afe09133f036d5fff88e772bbcc2c7d20ceb456e3233ab2b60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132824"
---
# <a name="running-32-bit-applications"></a>Esecuzione di applicazioni a 32 bit

WOW64 è l'emulatore x86 che consente alle applicazioni basate su Windows a 32 bit di essere eseguite senza problemi su Windows a 64 bit. In questo modo le applicazioni Windows a 32 bit (x86) possono essere eseguite senza problemi in applicazioni Windows a 64 bit (x64), nonché per applicazioni Windows a 32 bit (x86) e a 32 bit (ARM) per l'esecuzione senza problemi in Windows (ARM64) a 64 bit. WOW64 viene fornito con il sistema operativo e non deve essere abilitato in modo esplicito. Per altre informazioni, vedere [Dettagli sull'implementazione di WOW64.](wow64-implementation-details.md)

Il sistema isola le applicazioni a 32 bit dalle applicazioni a 64 bit, che includono la prevenzione di conflitti tra file e Registro di sistema. Sono supportate console, interfaccia utente grafica e applicazioni di servizio. Il sistema garantisce l'interoperabilità attraverso il limite 32/64 per scenari come taglia e incolla e COM. Tuttavia, i processi a 32 bit non possono caricare DLL a 64 bit per l'esecuzione e i processi a 64 bit non possono caricare DLL a 32 bit per l'esecuzione. Questa restrizione non si applica alle DLL caricate come file di dati o file di risorse di immagine. Per altre informazioni, vedere [**LoadLibraryEx.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa)

Un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (usare [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) se la destinazione è Windows 10). L'applicazione può ottenere informazioni aggiuntive sul processore usando la [**funzione GetNativeSystemInfo.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

Si noti che i Windows a 64 bit non supportano l'esecuzione di applicazioni Windows a 16 bit. Il motivo principale è che gli handle hanno 32 bit significativi su Windows. Pertanto, gli handle non possono essere troncati e passati alle applicazioni a 16 bit senza perdita di dati. I tentativi di avviare applicazioni a 16 bit hanno esito negativo con l'errore seguente: **ERRORE \_ BAD EXE \_ \_ FORMAT**.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Prestazioni e utilizzo della memoria in WOW64](performance-and-memory-consumption.md)
-   [Dettagli sull'implementazione di WOW64](wow64-implementation-details.md)
-   [Redirector del Registro di sistema](registry-redirector.md)
-   [File System Redirector](file-system-redirector.md)
-   [Gestione della memoria](memory-management.md)
-   [Affinità processori](processor-affinity.md)
-   [Comunicazione interprocesso](interprocess-communication.md)
-   [Installazione dell'applicazione](application-installation.md)
-   [Debug di WOW64](debugging-wow64.md)

 

 