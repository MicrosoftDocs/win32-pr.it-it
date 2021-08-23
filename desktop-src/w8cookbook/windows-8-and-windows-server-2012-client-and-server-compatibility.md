---
title: Compatibilità di client e server - Windows 8
description: Windows 8 compatibilità Windows Server 2012 client e server
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bbe52486339906d260fe623533cfbb871e97c07f914798990a5d16c51e5bbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593811"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a>Windows 8 compatibilità Windows Server 2012 client e server

Questa sezione descrive le modifiche del sistema operativo a cui è necessario prestare particolare attenzione a causa dei potenziali effetti sulle app esistenti e del modo in cui le nuove app devono essere progettate su client, server o su client e server. Di seguito è riportato l'elenco degli argomenti trattati in questa sezione, raggruppati per area di funzionalità:

**AppCompat**

-   Aggiornamento delle regole di rilevamento delle app di sicurezza
-   Determinazione dello stato degli shim
-   Le app server devono essere in grado di essere eseguite senza la shell grafica del server
-   I componenti del server Servizi Desktop remoto vengono rimossi da Windows 8
-   Modello di associazioni di tipi di file e protocolli
-   Desktop Activity Moderator
-   .NET Framework 4.5 è l'impostazione predefinita e .NET Framework 3.5 è facoltativa
-   Le app desktop potrebbero non essere visibili dopo l'avvio del Web browser predefinito
-   Modalità a contrasto elevato
-   Manifesto dell'app (eseguibile)
-   Il modello presente in coda è deprecato
-   Scenari di Assistente compatibilità programmi per Windows 8
-   Rimozione di desktop

**Archiviazione e file system**

-   Aggiornamento della compatibilità dei dischi in formato avanzato (4K)
-   Thin provisioning di unità logiche
-   L'archiviazione avanzata è ora facoltativa Windows ambiente di preinstallazione (WinPE) e SKU del server
-   È in corso la transizione di Servizio dischi virtuali alla Windows basata su Strumentazione gestione Windows (WMI) Windows Archiviazione API Gestione
-   Interfaccia utente delle versioni precedenti rimossa per i volumi locali
-   StorAHCI sostituisce MSAHCI
-   Windows 7 backup e ripristino deprecati
-   Trasferimenti di dati scaricati

**Altri**

-   Gestione finestre desktop è sempre on
-   Direct2D non supporta il rendering in metafile "rich" in Internet Explorer 9
-   Modifiche al supporto hardware legacy DX9
-   MSAA non è disponibile per le app Windows Store
-   La porta 3 è deprecata per i driver NDIS 6.30

 

 
