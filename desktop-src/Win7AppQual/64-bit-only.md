---
description: Solo a 64 bit
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29da3d00b457c7fe95ed7fe614991bc272968ad042b9c0360a14d48b1bf3461
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680261"
---
# <a name="64-bit-only"></a>Solo a 64 bit

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** - Windows Server 2008 R2  



## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Alta  






## <a name="description"></a>Descrizione

Windows Server 2008 R2 viene fornito solo con uno SKU a 64 bit. non sono disponibili SKU a 32 bit per la versione server del sistema operativo. Tuttavia, uno SKU a 32 bit continua a essere disponibile per il client Windows 7.

## <a name="manifestation-of-impact"></a>Impatto significativo

Ciò avrà effetto su tre aree:

-   Driver a 32 bit
-   Plug-in a 32 bit
-   Eseguibili a 16 bit

## <a name="solution-for-32-bit-drivers"></a>Soluzione per driver a 32 bit

Ricompilare i driver a 32 bit come driver a 64 bit firmati.

## <a name="solution-for-32-bit-plug-ins"></a>Soluzione per plug-in a 32 bit

WoW64, un emulatore x86, consente alle applicazioni basate su Windows a 32 bit di essere eseguite senza problemi in applicazioni a 64 bit Windows. WoW64 è ora una funzionalità facoltativa che è necessario installare se è necessario eseguire codice a 32 bit.

Il sistema isola le applicazioni a 32 bit dalle applicazioni a 64 bit, tra cui la prevenzione dei conflitti tra file e Registro di sistema. Sono supportate le applicazioni console, GUI e di servizio. Il sistema garantisce l'interoperabilità tra i limiti 32/64 per scenari come taglia e incolla e COM. Tuttavia, i processi a 32 bit non possono caricare DLL a 64 bit e i processi a 64 bit non possono caricare DLL a 32 bit. In genere è presente nei plug-in della shell scritti per Windows Explorer.

Un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione IsWow64Process. L'applicazione può ottenere informazioni aggiuntive sul processore usando la funzione GetNativeSystemInfo

Si noti che l'Windows a 64 bit non supporta l'esecuzione di applicazioni Windows a 16 bit. Il motivo principale è che gli handle hanno 32 bit significativi su un Windows a 64 bit. Pertanto, gli handle non possono essere troncati e passati alle applicazioni a 16 bit senza perdita di dati. I tentativi di avvio di applicazioni a 16 bit hanno esito negativo con l'errore seguente: ERROR \_ BAD \_ EXE \_ FORMAT.

## <a name="solution-for-16-bit-executables"></a>Soluzione per file eseguibili a 16 bit

L'Windows a 64 bit riconosce un numero limitato di programmi di installazione a 16 bit specifici e sostituisce una versione a 32 bit con portabilità. L'elenco delle sostituzioni viene archiviato nel Registro di sistema nella chiave seguente: HKEY LOCAL MACHINE Software Microsoft Windows NT CurrentVersion NtVdm64 È disponibile il supporto predefinito per diversi motori di installazione, inclusi i programmi di installazione \_ \_ \\ \\ \\ \\ \\ InstallShield 5.x. Si noti che il programma di installazione di Windows a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in un Windows a 64 bit.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Esecuzione di applicazioni a 32 bit](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Prestazioni e utilizzo della memoria](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [Dettagli sull'implementazione wow64](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Redirector del Registro di sistema](/windows/desktop/WinProg64/registry-redirector)
-   [File System Redirector](/windows/desktop/WinProg64/file-system-redirector)
-   [Gestione della memoria](/windows/desktop/WinProg64/memory-management)
-   [Affinità processori](/windows/desktop/WinProg64/processor-affinity)
-   [Comunicazione interprocesso](/windows/desktop/WinProg64/interprocess-communication)
-   [Installazione di applicazioni in sistemi a 64 bit](/windows/desktop/WinProg64/application-installation)
-   [Debug di WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**Funzione IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**Funzione GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
