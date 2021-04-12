---
description: .
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Solo 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3178a15ec0a138a73789233dd2d787964a96b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234000"
---
# <a name="64-bit-only"></a>Solo 64 bit

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -alta  






## <a name="description"></a>Descrizione

Windows Server 2008 R2 viene fornito solo con SKU a 64 bit. non sono disponibili SKU a 32 bit per la versione server del sistema operativo. Tuttavia, uno SKU a 32 bit continua a essere disponibile per il client di Windows 7.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Questa operazione avrà effetto su tre aree:

-   driver a 32 bit
-   plug-in a 32 bit
-   eseguibili a 16 bit

## <a name="solution-for-32-bit-drivers"></a>Soluzione per driver a 32 bit

Ricompilare i driver a 32 bit come driver 64 bit firmati.

## <a name="solution-for-32-bit-plug-ins"></a>Soluzione per plug-in a 32 bit

WoW64, un emulatore x86, consente alle applicazioni basate su Windows a 32 bit di funzionare facilmente in Windows a 64 bit. WoW64 è ora una funzionalità facoltativa che è necessario installare se è necessario eseguire codice a 32 bit.

Il sistema isola le applicazioni a 32 bit dalle applicazioni a 64 bit, inclusa la prevenzione dei conflitti tra file e registro di sistema. Sono supportate le applicazioni console, GUI e di servizio. Il sistema garantisce l'interoperabilità oltre il limite di 32/64 per scenari quali taglia e incolla e COM. Tuttavia, i processi a 32 bit non possono caricare le dll a 64 bit e i processi a 64 bit non possono caricare le dll a 32 bit. Questa operazione è comunemente visibile nei plug-in della shell scritti per Esplora risorse.

Un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione IsWow64Process. L'applicazione può ottenere ulteriori informazioni sul processore tramite la funzione GetNativeSystemInfo

Si noti che Windows a 64 bit non supporta l'esecuzione di applicazioni basate su Windows a 16 bit. Il motivo principale è che gli handle hanno 32 bit significativi in Windows a 64 bit. Non è pertanto possibile troncare gli handle e passarli a applicazioni a 16 bit senza perdita di dati. I tentativi di avvio delle applicazioni a 16 bit hanno esito negativo con l'errore seguente: errore del \_ \_ formato exe errato \_ .

## <a name="solution-for-16-bit-executables"></a>Soluzione per eseguibili a 16 bit

Windows a 64 bit riconosce un numero limitato di programmi programma di installazione a 16 bit specifici e sostituisce una versione a 32 bit portata. L'elenco di sostituzioni viene archiviato nel registro di sistema con la chiave seguente: HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 è disponibile il supporto incorporato per diversi motori di installazione, inclusi i programmi di installazione di InstallShield 5. x. Si noti che la Windows Installer a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Esecuzione di applicazioni a 32 bit](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Prestazioni e utilizzo di memoria](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [Dettagli di implementazione di WOW64](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Redirector del registro di sistema](/windows/desktop/WinProg64/registry-redirector)
-   [Redirector del file System](/windows/desktop/WinProg64/file-system-redirector)
-   [Gestione della memoria](/windows/desktop/WinProg64/memory-management)
-   [Affinità processori](/windows/desktop/WinProg64/processor-affinity)
-   [Comunicazione interprocesso](/windows/desktop/WinProg64/interprocess-communication)
-   [Installazione di applicazioni su sistemi a 64 bit](/windows/desktop/WinProg64/application-installation)
-   [Debug di WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**IsWow64Process (funzione)**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**GetNativeSystemInfo (funzione)**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
