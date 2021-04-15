---
title: Compatibilità con client e server-Windows 8
description: Compatibilità tra client e server di Windows 8 e Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "104335919"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a>Compatibilità tra client e server di Windows 8 e Windows Server 2012

In questa sezione vengono descritte le modifiche apportate al sistema operativo a cui è necessario prestare particolare attenzione a causa del potenziale impatto sulle app esistenti e del modo in cui le nuove app devono essere progettate nei client, nei server o nei client e nei server. Di seguito è riportato l'elenco degli argomenti trattati in questa sezione, raggruppati per area funzionale:

**AppCompat**

-   Aggiornamento delle regole di rilevamento delle app di sicurezza
-   Determinazione dello stato dello shim
-   Le app Server devono poter essere eseguite senza la shell grafica server
-   Componenti server RDS rimossi da Windows 8
-   Modello di tipo di file e associazioni di protocollo
-   Desktop Activity Moderator
-   .NET Framework 4,5 è il valore predefinito e .NET Framework 3,5 è facoltativo
-   Le applicazioni desktop potrebbero non essere visibili dopo l'avvio del Web browser predefinito
-   Modalità a contrasto elevato
-   Manifesto app (eseguibile)
-   Il modello presente in coda verrà deprecato
-   Scenari di compatibilità dei programmi per Windows 8
-   Gadget desktop rimossi

**Archiviazione e file System**

-   Aggiornamento della compatibilità del disco con formato avanzato (4K)
-   Thin provisioning di unità logiche
-   Archiviazione avanzata è ora facoltativa per Ambiente preinstallazione di Windows (WinPE) e SKU del server
-   Il servizio dischi virtuali sta passando all'API di gestione dell'archiviazione di Windows basata su Strumentazione gestione Windows (WMI)
-   Interfaccia utente delle versioni precedenti rimosse per i volumi locali
-   StorAHCI sostituisce MSAHCI
-   Backup e ripristino di Windows 7 deprecato
-   Trasferimenti dati scaricati

**Altri**

-   Gestione finestre desktop è sempre attiva
-   Direct2D non supporta il rendering in metafile "avanzati" in Internet Explorer 9
-   Modifiche al supporto hardware legacy di DX9
-   MSAA non è disponibile per le app di Windows Store
-   La porta 3 è deprecata per i driver NDIS 6,30

 

 
