---
title: Informazioni su BITS
description: Usare Servizio trasferimento intelligente in background (BITS) per trasferire i file in modo asincrono tra un client e un server.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Servizio trasferimento intelligente in background, descritto
- coda di trasferimento BITS
- bits coda di trasferimento, limitazione
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 53693b7087d647e8d6e89a8c81e09895dc3866b964642475466bbf8f52ddbae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529281"
---
# <a name="about-bits"></a>Informazioni su BITS

Usare Servizio trasferimento intelligente in background (BITS) per scaricare o caricare file in server Web HTTP o file server SMB. 

BITS continua a trasferire i file dopo la chiusura di un'applicazione finché l'utente che ha avviato il trasferimento rimane connesso e viene mantenuta una connessione di rete. BITS non forza una connessione di rete. BITS riprende i trasferimenti dopo che una connessione di rete persa è stata ristabilita o dopo che un utente che si era disconnesso si è connesso nuovamente. Per altre informazioni, vedere [Utenti e connessioni di rete.](users-and-network-connections.md)

BITS è importante per i costi e la congestione correnti della rete, in modo che un processo in background interferisca il meno possibile con l'esperienza in primo piano dell'utente. BITS usa la [larghezza](network-bandwidth.md) di banda di rete inattiva per trasferire i file e aumenterà o ridurrà la velocità di trasferimento dei file in base alla quantità di larghezza di banda di rete inattiva disponibile. Se un'applicazione di rete utilizza una quantità maggiore di larghezza di banda, BITS diminuisce la velocità di trasferimento per conservare l'esperienza interattiva dell'utente. BITS usa criteri di trasferimento specificati [dall'app](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) per impedire il trasferimento di file in connessioni di rete costose.

BITS è importante anche per l'utilizzo dell'energia elettrica. A partire dal Aggiornamento di Windows 10 (maggio 2019), BITS trasferisce i file quando il computer è in modalità [Standby](/windows-hardware/design/device-experiences/modern-standby) moderno e il computer è collegato.

L'applicazione BITS può usare i diversi livelli di priorità [BITS](/windows/desktop/api/Bits/ne-bits-bg_job_priority) per consentire a BITS di scegliere in modo intelligente i processi di trasferimento da eseguire. I processi con priorità più alta hanno la precedenza rispetto a quelli con priorità più bassa. I processi con lo stesso livello di priorità condividono il tempo di trasferimento, in modo che un processo di grandi dimensioni non blocchi i processi più piccoli nella coda di trasferimento. I processi con priorità più bassa non ricevono il tempo di trasferimento finché tutti i processi con priorità più alta non vengono completati o non sono in stato di errore.

BITS usa Windows BranchCache per il peer caching. Per altre informazioni, vedere Panoramica [di BranchCache.](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))

Gli sviluppatori della piattaforma UWP (Universal Windows Platform) devono usare il [Windows. API Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e non API BITS.

Esistono tre tipi di processi [**di trasferimento.**](/windows/desktop/api/Bits/ne-bits-bg_job_type) Un processo di download scarica i file nel client, un processo di caricamento carica un file nel server e un processo upload-reply carica un file nel server e riceve un file di risposta dall'applicazione server.

Gli argomenti seguenti forniscono informazioni più dettagliate su BITS:

-   [autenticazione](authentication.md)
-   [Ciclo di vita di un processo BITS](life-cycle-of-a-bits-job.md)
-   [Utenti e connessioni di rete](users-and-network-connections.md)
-   [Larghezza di banda di rete](network-bandwidth.md)
-   [Criteri di gruppo](group-policies.md)
-   [Account del servizio e BITS](service-accounts-and-bits.md)
-   [Token helper per processi di trasferimento BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Coerenza del trasferimento di file](file-transfer-consistency.md)
-   [Requisiti HTTP per i download BITS](http-requirements-for-bits-downloads.md)
-   [Requisiti IIS per i caricamenti BITS](iis-requirements-for-bits-uploads.md)
-   [Pulizia della directory virtuale](virtual-directory-cleanup.md)
-   [BITS e Ripristino configurazione di sistema](bits-and-system-restore.md)
-   [Tipo di avvio BITS](bits-startup-type.md)
-   [Condivisione connessione Internet](internet-connection-sharing.md)
-   [Peer Caching](peer-caching.md)
-   [Sicurezza BITS, token e account amministratore](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Usare le interfacce BITS [per scrivere applicazioni che](bits-interfaces.md) creano e monitorano i processi di trasferimento. Per informazioni dettagliate sull'uso delle interfacce BITS, vedere [Uso di BITS.](using-bits.md)