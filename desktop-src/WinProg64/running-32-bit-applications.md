---
title: Esecuzione di applicazioni a 32 bit
description: Eseguire facilmente applicazioni basate su Windows a 32 bit su Windows a 64 bit con l'emulatore WOW64 x86. Scopri anche il direttore del registro di sistema, il redirector file system, l'installazione di applicazioni su sistemi a 64 bit e il debug di WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- Programmazione Windows WOW64 a 64 bit
- Programmazione Windows WOW64 a 64 bit, informazioni
- applicazioni a 32 bit sulla programmazione Windows a 64 bit di Windows a 64 bit
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, WOW64 vedere WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963136"
---
# <a name="running-32-bit-applications"></a>Esecuzione di applicazioni a 32 bit

WOW64 è l'emulatore x86 che consente l'esecuzione delle applicazioni basate su Windows a 32 bit su Windows a 64 bit. Questo consente di eseguire facilmente applicazioni Windows a 32 bit (x86) in Windows a 64 bit (x64), oltre che per applicazioni Windows a 32 bit (x86) e a 32 bit (ARM), in modo che vengano eseguite facilmente in Windows ARM64 (64 bit). WOW64 viene fornito con il sistema operativo e non è necessario che sia abilitato in modo esplicito. Per ulteriori informazioni, vedere la pagina relativa ai [Dettagli di implementazione di WOW64](wow64-implementation-details.md).

Il sistema isola le applicazioni a 32 bit dalle applicazioni a 64 bit, inclusa la prevenzione dei conflitti tra file e registro di sistema. Sono supportate le applicazioni console, GUI e di servizio. Il sistema garantisce l'interoperabilità oltre il limite di 32/64 per scenari quali taglia e incolla e COM. Tuttavia, i processi a 32 bit non possono caricare le dll a 64 bit per l'esecuzione e i processi a 64 bit non possono caricare le dll a 32 bit per l'esecuzione. Questa restrizione non è valida per le DLL caricate come file di dati o file di risorse immagine; Per ulteriori informazioni, vedere [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (usare [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) se la destinazione è Windows 10). L'applicazione può ottenere ulteriori informazioni sul processore utilizzando la funzione [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Si noti che Windows a 64 bit non supporta l'esecuzione di applicazioni basate su Windows a 16 bit. Il motivo principale è che gli handle hanno 32 bit significativi in Windows a 64 bit. Non è pertanto possibile troncare gli handle e passarli a applicazioni a 16 bit senza perdita di dati. I tentativi di avvio delle applicazioni a 16 bit hanno esito negativo con l'errore seguente: **errore del \_ \_ \_ formato exe errato**.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Prestazioni e utilizzo di memoria in WOW64](performance-and-memory-consumption.md)
-   [Dettagli di implementazione di WOW64](wow64-implementation-details.md)
-   [Redirector del registro di sistema](registry-redirector.md)
-   [Redirector del file System](file-system-redirector.md)
-   [Gestione della memoria](memory-management.md)
-   [Affinità processori](processor-affinity.md)
-   [Comunicazione interprocesso](interprocess-communication.md)
-   [Installazione dell'applicazione](application-installation.md)
-   [Debug di WOW64](debugging-wow64.md)

 

 