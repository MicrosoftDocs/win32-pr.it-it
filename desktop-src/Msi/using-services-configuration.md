---
description: La configurazione dei servizi consente Windows programma di installazione di personalizzare i servizi in un computer.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Uso della configurazione dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe1e34cce317ee00c3cc9d6ee4aac449e500499dc2dee4e97df65ba91bca2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012706"
---
# <a name="using-services-configuration"></a>Uso della configurazione dei servizi

La configurazione dei servizi consente Windows programma di installazione di personalizzare [i servizi](../services/services.md) in un computer. Gli sviluppatori possono creare un pacchetto di Windows Installer per installare, arrestare, avviare ed eliminare servizi durante un'installazione usando le tabelle [ServiceControl](servicecontrol-table.md) e [ServiceInstall](serviceinstall-table.md) e le azioni [InstallServices](installservices-action.md), [StopServices](stopservices-action.md) [e DeleteServices.](deleteservices-action.md)

A partire da pacchetti scritti per Windows Installer 5.0, gli sviluppatori possono anche usare l'azione standard [MsiConfigureServices](msiconfigureservices-action.md) e la tabella [MsiServiceConfig](msiserviceconfig-table.md) per configurare le opzioni di personalizzazione del servizio estese disponibili con Windows 7 e Windows Server 2008 R2 e Windows Vista e Windows Server 2008. I pacchetti di installazione esistenti scritti per le versioni del programma di installazione di Windows che non includeva la tabella MsiServiceConfig possono comunque essere installati usando Windows Installer 5.0. La funzionalità di configurazione dei servizi del programma di installazione di Windows non può configurare gli account del servizio di rete, installare processi host del servizio condiviso (svchost) o riavviare i servizi arrestati durante l'installazione.

**Windows XP e Windows Server 2003 o versioni precedenti:** Non supportato. Le tabelle di configurazione del servizio e le azioni standard sono disponibili a partire da Windows Installer 5.0 in esecuzione in Windows 7 e Windows Server 2008 R2 e Windows Installer 4.5 in esecuzione in Windows Vista e Windows Server 2008.

È necessario includere [l'azione MsiConfigureServices](msiconfigureservices-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) per richiedere le configurazioni del servizio specificate nella [tabella MsiServiceConfig](msiserviceconfig-table.md). Il Windows programma di installazione usa le informazioni nella tabella MsiServiceConfig solo quando l'azione standard MsiConfigureServices è inclusa in una tabella di sequenza. L'azione standard MsiConfigureServices usa anche le informazioni nelle [tabelle ServiceControl](servicecontrol-table.md) [e ServiceInstall.](serviceinstall-table.md)

Per richiedere che il sistema conseglie solo i privilegi necessari a un determinato servizio, specificare il servizio e l'opzione di configurazione **SERVICE \_ CONFIG REQUIRED \_ \_ PRIVILEGES \_ INFO** nella tabella [MsiServiceConfig](msiserviceconfig-table.md). Rimuovere i privilegi non necessari dal token di processo del servizio. Questa opzione può essere usata per configurare i servizi eseguiti nel contesto di sicurezza degli account utente del servizio LocalSystem, LocalService [o](../services/service-user-accounts.md)NetworkService .

Per richiedere al sistema di ritardare l'avvio automatico di un servizio per un periodo di tempo successivo all'avvio di tutti gli altri servizi di avvio automatico, specificare il servizio e l'opzione **SERVICE \_ CONFIG \_ DELAYED AUTO \_ \_ START** nella tabella [MsiServiceConfig](msiserviceconfig-table.md). Il servizio ritardato deve essere installato dal pacchetto corrente con SERVICE AUTO START specificato nella tabella ServiceInstall oppure il servizio deve essere già installato come servizio \_ \_ di avvio automatico. [](serviceinstall-table.md)

Per richiedere al sistema di riservare una risorsa per l'uso esclusivo di un determinato servizio, specificare il servizio, il tipo di SID del servizio e l'opzione di configurazione **SERVICE \_ CONFIG SERVICE \_ \_ SID \_ INFO** nella tabella [MsiServiceConfig](msiserviceconfig-table.md). Aggiungere il SID del servizio all'elenco di controllo di accesso (ACL) della risorsa per la risorsa.

Per richiedere che [Gestione controllo servizi](../services/service-control-manager.md) attenda dopo l'invio della notifica SERVICE CONTROL **\_ \_ PRESHUTDOWN** a un servizio, eseguire le operazioni seguenti. Specificare il servizio, il tempo di attesa di Gestione configurazione SCM e l'opzione di configurazione **SERVICE \_ CONFIG \_ PRESHUTDOWN \_ INFO** nella [tabella MsiServiceConfig](msiserviceconfig-table.md).

Per configurare quando il sistema deve eseguire azioni dopo l'errore di un servizio, specificare il servizio e l'opzione **SERVICE CONFIG FAILURE ACTIONS \_ \_ \_ \_ FLAG** nella tabella [MsiServiceConfig](msiserviceconfig-table.md). Aggiungere le azioni da eseguire alla [tabella MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

Per altre informazioni sulle funzionalità di personalizzazione dei servizi estese introdotte con i sistemi operativi Windows Vista e Windows Server 2008, vedere Service [Changes for Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
