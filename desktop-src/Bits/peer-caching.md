---
title: Peer caching
description: A partire da Servizio trasferimento intelligente in background (BITS) 4,0, il servizio BITS è stato esteso per consentire la memorizzazione nella cache peer a livello di subnet per i dati URL scaricati usando Windows BranchCache.
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300030"
---
# <a name="peer-caching"></a>Peer caching

A partire da Servizio trasferimento intelligente in background (BITS) 4,0, il servizio BITS è stato esteso per consentire la memorizzazione nella cache peer a livello di subnet per i dati URL scaricati usando Windows BranchCache. I client BITS possono recuperare i dati da altri computer nella propria subnet che hanno già scaricato i dati, anziché recuperare i dati dai server remoti. Per ulteriori informazioni su Windows BranchCache, vedere [Panoramica di BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Se un amministratore abilita Windows BranchCache sui computer client e server di un'organizzazione tramite criteri di gruppo o impostazioni di configurazione locali, BITS utilizzerà Windows BranchCache per i trasferimenti di dati.

-   [Configurazione per la memorizzazione nella cache peer 4,0 BITS](#configuration-for-bits-40-peer-caching)
-   [Disabilitazione di Windows BranchCache](#disabling-windows-branchcache)
-   [Verifica e monitoraggio](#verification-and-monitoring)
-   [Peer caching in BITS 3,0](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>Configurazione per la memorizzazione nella cache peer 4,0 BITS

La configurazione seguente è necessaria per il funzionamento della memorizzazione nella cache peer in BITS 4,0:

-   Windows BranchCache deve essere abilitato sul client tramite un criterio di gruppo o impostazioni di configurazione locale. Per ulteriori informazioni, vedere la pagina relativa alla [configurazione del client BranchCache](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10)).
    > [!Note]  
    > Per impostazione predefinita, la funzionalità Windows BranchCache è disabilitata.

     

-   La funzionalità Windows BranchCache è un componente facoltativo che deve essere installato nel server. Per ulteriori informazioni, vedere la pagina relativa alla [configurazione del server BranchCache](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
-   Il server deve inoltre abilitare la funzionalità Windows BranchCache tramite criteri di gruppo o impostazioni di configurazione locale. Per ulteriori informazioni, vedere la pagina relativa alla [configurazione del server BranchCache](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
    > [!Note]  
    > Per impostazione predefinita, la funzionalità Windows BranchCache è disabilitata.

     

I criteri di gruppo BITS predefiniti consentono la memorizzazione nella cache peer. Se Windows BranchCache è abilitato a livello globale in un computer, questa funzionalità è abilitata anche per i processi di trasferimento BITS. Per ulteriori informazioni sui criteri di gruppo specifici per BITS, vedere [criteri di gruppo](group-policies.md).

## <a name="disabling-windows-branchcache"></a>Disabilitazione di Windows BranchCache

Un amministratore può utilizzare criteri di gruppo per disabilitare l'utilizzo di Windows BranchCache. Vedere [criteri di gruppo](group-policies.md). Se Windows BranchCache è disabilitato, i client BITS recupereranno i dati solo da server remoti.

Un'applicazione può inoltre disabilitare Windows BranchCache in base a ogni processo chiamando il metodo [**IBackgroundCopyJob4:: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) e impostando il flag **di \_ disabilitazione della \_ \_ cache del ramo di BG** .

> [!Note]  
> Queste impostazioni non influiscono sull'utilizzo di Windows BranchCache da parte di applicazioni diverse da BITS. Queste impostazioni non si applicano ai trasferimenti BITS tramite SMB. BITS non controlla le impostazioni per i trasferimenti di Windows BranchCache tramite SMB.

 

## <a name="verification-and-monitoring"></a>Verifica e monitoraggio

Esistono diversi modi per verificare e monitorare le statistiche di peer caching. Gli amministratori possono chiamare il metodo [**IBackgroundCopyFile4:: GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) per eseguire una query sulla quantità di dati scaricati da peer e da server di origine. Gli amministratori possono inoltre controllare il registro eventi per l' [ID evento 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10)), che fornisce informazioni specifiche del processo.

La funzionalità Windows BranchCache fornisce inoltre diversi meccanismi per verificare e monitorare le statistiche relative alla memorizzazione nella cache peer. Per ulteriori informazioni, vedere [Verifica e monitoraggio](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) e [contatori delle prestazioni](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10)).

Il modello di memorizzazione nella cache peer che utilizza Windows BranchCache sostituisce il modello di memorizzazione nella cache peer utilizzato nei bit 3,0. Per ulteriori informazioni su Windows BranchCache, vedere gli argomenti seguenti:

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [BranchCache Overview](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Servizi di Windows 7](../win7devguide/services.md)
-   [API di distribuzione peer](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>Peer caching in BITS 3,0

> [!Note]  
> A partire da Windows 7, il modello BITS 3,0 Caching peer è deprecato. Se è installato BITS 4,0, il modello di memorizzazione nella cache dei peer 3,0 BITS non è disponibile.

 

Se l'amministratore abilita la memorizzazione nella cache peer e il processo consente il download del contenuto da un peer, BITS tenterà di scaricare il contenuto da uno o più peer. Il download da un peer è molto più veloce del download del contenuto da Internet. Il peer caching è disabilitato per impostazione predefinita e i processi devono consentire in modo esplicito il download del contenuto dai peer. Un amministratore può utilizzare criteri di gruppo per abilitare la memorizzazione nella cache peer. Dopo aver abilitato la memorizzazione nella cache peer, l'amministratore può disabilitare il download da un peer o la conservazione di contenuto a un peer.

Un'applicazione può anche abilitare la memorizzazione nella cache peer chiamando il metodo [**IBitsPeerCacheAdministration:: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) . Tuttavia, queste impostazioni vengono sostituite dalle impostazioni di criteri di gruppo, se impostate.

Quando la memorizzazione nella cache peer è abilitata, BITS crea un elenco di peer che si trovano nella stessa subnet e appartengono allo stesso dominio. L'elenco non includerà peer da un dominio trusted. La memorizzazione nella cache peer può essere abilitata solo in un ambiente di dominio.

BITS individua i peer eseguendo le operazioni seguenti:

-   Ascolto dei server peer che annunciano se stessi. Un server peer si annuncia all'avvio. BITS consente di aggiungere il server peer all'elenco se il client necessita di più peer nell'elenco.
-   Trasmissione di una richiesta per i server peer quando sono necessari più peer nell'elenco di peer. I server peer disponibili per gestire il contenuto rispondono alla richiesta.

BITS rimuove i server peer dall'elenco peer se il server esegue le operazioni seguenti:

-   Autenticazione non riuscita
-   Offline (non disponibile) per troppo tempo
-   Fornisce un certificato con errori

Quando un processo richiede contenuto da un peer, BITS sceglie in modo casuale un subset di peer dall'elenco peer e li chiede se dispone del contenuto. BITS può scaricare il contenuto solo da server peer autenticati. Il client e il server eseguono inizialmente l'autenticazione reciproca tramite Kerberos e quindi scambiano i certificati autofirmati per l'autenticazione durante l'individuazione e il download del contenuto.

BITS scarica il contenuto dal primo peer autenticato per rispondere alla richiesta. Se un peer non contiene tutto il contenuto, BITS scaricherà ciò che può fare da uno o più peer prima di scaricare il resto dal server di origine. Se nessuno dei peer presenta il contenuto o si verifica un errore durante il download da un peer, BITS scarica il contenuto dal server di origine.

Il contenuto scaricato diventa disponibile per essere utilizzato ad altri peer solo dopo che l'applicazione ha convalidato il contenuto dei file. Se il file non viene convalidato in modo esplicito, il file viene convalidato in modo implicito quando l'applicazione completa il processo.

Per impostazione predefinita, un server peer può gestire il contenuto solo con tre client simultaneamente. Se il server è attualmente occupato a servire tre client, si verifica un ritardo nella risposta ad altre richieste. BITS limita la larghezza di banda usata per gestire il contenuto a 1 Mbps. Per modificare il limite, è possibile usare i criteri di gruppo [MaxBandwidthServed](group-policies.md) .

> [!Note]  
> Questa funzionalità è supportata solo nelle reti di dominio. la memorizzazione nella cache peer non è supportata nei gruppi di lavoro o nelle reti domestiche.

Vedere anche [amministrazione della peer cache](/windows/desktop/Bits/administering-the-peer-cache)
 

 

 