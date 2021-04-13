---
description: La configurazione dei servizi consente all'Windows Installer di personalizzare i servizi in un computer.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Uso della configurazione dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6e3040d51b1056a370490fc5328a6bafe07555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484188"
---
# <a name="using-services-configuration"></a>Uso della configurazione dei servizi

La configurazione dei servizi consente all'Windows Installer di personalizzare i [Servizi](../services/services.md) in un computer. Gli sviluppatori possono creare un pacchetto di Windows Installer per installare, arrestare, avviare ed eliminare servizi durante un'installazione tramite le tabelle [ServiceControl](servicecontrol-table.md) e [ServiceInstall](serviceinstall-table.md) e le azioni [InstallServices](installservices-action.md), [StopServices](stopservices-action.md) e [DeleteServices](deleteservices-action.md) .

A partire dai pacchetti scritti per Windows Installer 5,0, gli sviluppatori possono anche usare l'azione standard [MsiConfigureServices](msiconfigureservices-action.md) e la [tabella MsiServiceConfig](msiserviceconfig-table.md) per configurare le opzioni di personalizzazione del servizio estese disponibili con Windows 7 e Windows Server 2008 R2 e Windows Vista e Windows Server 2008. I pacchetti di installazione esistenti scritti per le versioni del Windows Installer che non includevano la tabella MsiServiceConfig possono essere ancora installati con Windows Installer 5,0. La funzionalità di configurazione dei servizi del Windows Installer non è in grado di configurare gli account del servizio di rete, installare i processi dell'host del servizio condiviso (SVCHOST) o riavviare i servizi arrestati come parte dell'installazione.

**Windows XP e Windows Server 2003 o versioni precedenti:** Non supportato. Le tabelle di configurazione dei servizi e le azioni standard sono disponibili a partire da Windows Installer 5,0 in esecuzione su Windows 7 e Windows Server 2008 R2 e Windows Installer 4,5 in esecuzione in Windows Vista e Windows Server 2008.

Per richiedere le configurazioni del servizio specificate nella [tabella MsiServiceConfig](msiserviceconfig-table.md), è necessario includere l'azione [MsiConfigureServices](msiconfigureservices-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) . Il Windows Installer utilizza le informazioni nella tabella MsiServiceConfig solo quando l'azione MsiConfigureServices standard è inclusa in una tabella di sequenza. L'azione standard MsiConfigureServices usa anche le informazioni contenute nelle tabelle [ServiceControl](servicecontrol-table.md) e [ServiceInstall](serviceinstall-table.md) .

Per richiedere che il sistema fornisca solo i privilegi necessari per un particolare servizio, specificare l'opzione di configurazione servizio e configurazione del **servizio \_ \_ richiesta \_ \_ informazioni privilegi** nella [tabella MsiServiceConfig](msiserviceconfig-table.md). Rimuovere i privilegi non necessari dal token del processo del servizio. Questa opzione può essere utilizzata per configurare i servizi eseguiti nel contesto di sicurezza degli [account utente del servizio](../services/service-user-accounts.md)LocalSystem, LocalService o NetworkService.

Per richiedere che il sistema ritardi l'avvio automatico di un servizio per un periodo di tempo dopo l'avvio di tutti gli altri servizi di avvio automatico, specificare il servizio e l'opzione di **\_ \_ \_ \_ avvio automatico ritardato della configurazione del servizio** nella [tabella MsiServiceConfig](msiserviceconfig-table.md). Il servizio in fase di ritardo deve essere installato dal pacchetto corrente con l' \_ avvio automatico del servizio \_ specificato nella tabella [ServiceInstall](serviceinstall-table.md) o il servizio deve essere già installato come servizio di avvio automatico.

Per richiedere al sistema di riservare una risorsa per l'uso esclusivo di un determinato servizio, specificare il servizio, il tipo di SID del servizio e l'opzione di configurazione Service **\_ config \_ Service \_ \_ info SID** nella [tabella MsiServiceConfig](msiserviceconfig-table.md). Aggiungere il SID del servizio all'elenco di controllo di accesso (ACL) della risorsa.

Per richiedere che [Gestione controllo servizi](../services/service-control-manager.md) (SCM) attenda dopo l'invio della notifica di **\_ \_ prechiusura del controllo** del servizio a un servizio, eseguire le operazioni seguenti. Specificare il servizio, l'intervallo di tempo in cui il controllo SCM deve attendere e l'opzione di configurazione **Service \_ config \_ preshutdown \_ info** nella [tabella MsiServiceConfig](msiserviceconfig-table.md).

Per configurare quando il sistema deve eseguire azioni dopo l'errore di un servizio, specificare l'opzione relativa al servizio e alla configurazione del servizio non **\_ \_ riuscito \_ \_** nella [tabella MsiServiceConfig](msiserviceconfig-table.md). Aggiungere le azioni da eseguire alla [tabella MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

Per ulteriori informazioni sulle funzionalità di personalizzazione dei servizi estese introdotte con i sistemi operativi Windows Vista e Windows Server 2008, vedere [modifiche ai servizi per Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
