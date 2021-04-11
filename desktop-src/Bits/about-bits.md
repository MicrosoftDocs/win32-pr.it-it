---
title: Informazioni su BITS
description: Usare Servizio trasferimento intelligente in background (BITS) per trasferire file in modo asincrono tra un client e un server.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Servizio trasferimento intelligente in background, descritto
- BIT coda di trasferimento
- BIT della coda di trasferimento, limitazione
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b1ac0f587b496692ec1c2e62be06c0e64766a205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117830"
---
# <a name="about-bits"></a>Informazioni su BITS

Usare Servizio trasferimento intelligente in background (BITS) per scaricare file o caricare file in server Web HTTP o file server SMB. 

BITS continua a trasferire i file dopo la chiusura di un'applicazione fino a quando l'utente che ha avviato il trasferimento rimane connesso e viene mantenuta una connessione di rete. BITS non impone la connessione di rete. BITS riprende i trasferimenti dopo che è stata ristabilita una connessione di rete persa o dopo un utente che ha disconnesso i log. Per ulteriori informazioni, vedere [utenti e connessioni di rete](users-and-network-connections.md).

BITS indica il costo e la congestione della rete correnti, in modo che un processo in background interferisca il minor possibile con l'esperienza in primo piano dell'utente. BITS usa la [larghezza di banda di rete](network-bandwidth.md) inattiva per trasferire i file e aumenta o diminuisce la velocità di trasferimento dei file in base alla quantità di larghezza di banda di rete inattiva disponibile. Se un'applicazione di rete utilizza una quantità maggiore di larghezza di banda, BITS diminuisce la velocità di trasferimento per conservare l'esperienza interattiva dell'utente. BITS usa i criteri di [trasferimento](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) specificati dall'app per impedire il trasferimento di file su connessioni di rete costose.

BITS è anche consapevole dell'utilizzo dell'energia elettrica. A partire da Windows 10 può 2019 aggiornamento, BITS trasferirà i file quando il computer è in modalità [standby moderna](/windows-hardware/design/device-experiences/modern-standby) e il computer è collegato.

L'applicazione BITS può utilizzare i diversi [livelli di priorità](/windows/desktop/api/Bits/ne-bits-bg_job_priority) bits per consentire a bits di selezionare in modo intelligente i processi di trasferimento da eseguire. I processi con priorità più alta hanno la precedenza rispetto a quelli con priorità più bassa. I processi con lo stesso livello di priorità condividono il tempo di trasferimento, in modo che un processo di grandi dimensioni non blocchi i processi più piccoli nella coda di trasferimento. I processi con priorità più bassa non ricevono il tempo di trasferimento finché tutti i processi con priorità più alta non vengono completati o non sono in stato di errore.

BITS utilizza Windows BranchCache per la memorizzazione nella cache peer. Per ulteriori informazioni, vedere [Panoramica di BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Gli sviluppatori piattaforma UWP (Universal Windows Platform) (UWP) devono usare l'API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e non l'API BITS.

Sono disponibili tre tipi di [**processi di trasferimento**](/windows/desktop/api/Bits/ne-bits-bg_job_type). Un processo di download Scarica i file nel client, un processo di caricamento carica un file nel server e un processo di caricamento-risposta carica un file nel server e riceve un file di risposta dall'applicazione server.

Negli argomenti seguenti vengono fornite informazioni più dettagliate sui bit:

-   [autenticazione](authentication.md)
-   [Ciclo di vita di un processo BITS](life-cycle-of-a-bits-job.md)
-   [Utenti e connessioni di rete](users-and-network-connections.md)
-   [Larghezza di banda di rete](network-bandwidth.md)
-   [Criteri di gruppo](group-policies.md)
-   [Account del servizio e BITS](service-accounts-and-bits.md)
-   [Token helper per i processi di trasferimento BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Coerenza del trasferimento di file](file-transfer-consistency.md)
-   [Requisiti HTTP per i download BITS](http-requirements-for-bits-downloads.md)
-   [Requisiti di IIS per i caricamenti BITS](iis-requirements-for-bits-uploads.md)
-   [Pulizia directory virtuale](virtual-directory-cleanup.md)
-   [BITS e ripristino del sistema](bits-and-system-restore.md)
-   [Tipo di avvio BITS](bits-startup-type.md)
-   [Condivisione connessione Internet](internet-connection-sharing.md)
-   [Peer caching](peer-caching.md)
-   [Sicurezza BITS, token e account amministratore](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Utilizzare le [interfacce](bits-interfaces.md) bits per scrivere applicazioni che creano e monitorano i processi di trasferimento. Per informazioni dettagliate sull'uso delle interfacce BITS, vedere [uso di BITS](using-bits.md).