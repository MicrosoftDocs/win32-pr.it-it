---
description: L'elenco seguente descrive le aree di funzionalità nuove e aggiornate per Windows Server 2012 e Windows Server 2012 R2. Per altre informazioni sulle nuove tecnologie Windows 8 e Windows 8.1, vedere Windows 8 e Windows 8.1 tecnologie.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Novità: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df654e7c448ef4e4f6f4f1599204883cad11bf5e56ccd13c47c76d204f7587f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867503"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Novità: Windows Server 2012 R2 & Windows Server 2012

L'elenco seguente descrive le aree di funzionalità nuove e aggiornate per Windows Server 2012 e Windows Server 2012 R2. Per altre informazioni sulle nuove tecnologie Windows 8 e Windows 8.1, vedere tecnologie [Windows 8 e Windows 8.1.](/previous-versions/windows/desktop/whatsnew/windows-8-technologies)

## <a name="whats-new-for-windows-server-2012-r2"></a>Novità di Windows Server 2012 R2

-   [Deduplicazione dati](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    La deduplicazione dei dati individua e rimuove la duplicazione all'interno dei dati in un volume, assicurando al tempo stesso che i dati rimangano corretti e completi. In questo modo è possibile memorizzare un maggior quantitativo di dati dei file in meno spazio del volume. Per Windows Server 2012 R2, sono stati attivati diversi parametri e codici di errore ed è stata aggiunta la classe [**\_ MSFT DedupFileMetadata.**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata)

-   [Registrazione inventario software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Novità** Registrazione inventario software raccoglie i dati sulle licenze relative al software installato in un server Windows e fornisce l'accesso remoto ai dati in modo che possano essere aggregati facilmente da un data center.

-   [Server di destinazione iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    L'API Server di destinazione iSCSI fornisce provider di Strumentazione gestione Windows (WMI) per la gestione di Microsoft Server di destinazione iSCSI, ad esempio la creazione di dischi virtuali, e per presentarli al client. Sono state aggiunte diverse nuove funzionalità per Windows Server 2012 R2.

-   [Registrazione per la gestione dei dispositivi mobili](../mdmreg/mobile-device-management-registration-portal.md)

    **Novità** Si sta sviluppando una tendenza del settore in cui i dipendenti connettono i propri dispositivi di mobile computing personali alla rete aziendale e alle risorse (in locale o tramite il cloud) per eseguire le attività aziendali. Questa tendenza richiede il supporto per una configurazione semplice della rete e delle risorse, in modo che i dipendenti possano registrare i dispositivi personali con l'azienda per scopi aziendali. Le applicazioni e la tecnologia per supportare una configurazione semplice devono anche consentire ai professionisti IT di gestire i rischi associati alla connessione di dispositivi non controllato alla rete aziendale. La registrazione di Gestione di dispositivi mobili (MDM) registra un dispositivo in un servizio di gestione.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell è una shell della riga di comando basata su attività e un linguaggio di scripting progettato appositamente per l'amministrazione del sistema. Novità di Windows Server 2012 R2, Windows PowerShell v4 supporta Desired State Configuration, una nuova piattaforma di gestione di Windows PowerShell che consente la distribuzione e la gestione dei dati di configurazione per i servizi software e la gestione dell'ambiente in cui vengono eseguiti questi servizi.

## <a name="whats-new-for-windows-server-2012"></a>Novità di Windows Server 2012

-   [Windows Clustering](/previous-versions/windows/desktop/mscs/windows-clustering)

    Windows Il clustering consente di gestire sia i cluster con bilanciamento del carico di rete che i cluster di failover. In questa versione sono state aggiunte diverse nuove funzionalità, tra cui nuove funzionalità di gestione dei gruppi, proprietà comuni e integrazione con WMI.

-   [Registrazione accesso utenti](/previous-versions/windows/desktop/ual/user-access-logging)

    **Novità** Registrazione accesso utenti è un framework comune che consente ai ruoli Windows Server di segnalare le rispettive metriche di utilizzo. Questo framework di Registrazione utenti è un componente fondamentale e fondamentale della soluzione di gestione delle licenze più ampia.

-   [Gestione remota Windows](../winrm/portal.md)

    Gestione remota Windows (WinRM) è l'implementazione di Microsoft del protocollo WS-Management, un protocollo standard basato su SOAP (Simple Object Access Protocol) adatto al firewall che consente l'interoperabilità di hardware e sistemi operativi di fornitori diversi. Windows Server 2012 include una serie di API di connessione incentrate sull'interazione con le istanze e le shell in esecuzione.

-   [Windows Infrastruttura di gestione](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Novità** Le funzionalità di Windows Management Infrastructure (MI) rappresentano la versione più recente delle tecnologie di Strumentazione gestione Windows (WMI), basate sullo standard CIM di DMTF (Distributed Management Task Force). Mi è completamente compatibile con le versioni precedenti di WMI e offre una serie di funzionalità e vantaggi che rendono più semplice che mai la progettazione e lo sviluppo di provider e client.

-   [Deduplicazione dati](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Novità** La deduplicazione dei dati individua e rimuove la duplicazione all'interno dei dati in un volume, assicurando al tempo stesso che i dati rimangano corretti e completi. In questo modo è possibile memorizzare un maggior quantitativo di dati dei file in meno spazio del volume.

-   [Server di destinazione iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Novità** L'API Server di destinazione iSCSI fornisce provider di Strumentazione gestione Windows (WMI) per la gestione di Microsoft Server di destinazione iSCSI, ad esempio la creazione di dischi virtuali, e per presentarli al client.

-   [Provider NFS per WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Novità** Il provider WMI NFS consente di gestire le impostazioni client, le condivisioni file, i netgroup e i gruppi di client NFS.

-   [File offline](../devnotes/offline-files.md)

    L File offline API consente alle applicazioni di controllare e monitorare il comportamento dei File offline a livello di codice. Windows Server 2012 aggiunge le [**funzioni OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) [**e RenameItem.**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem)

-   [Gestione SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Novità** La libreria SMB API Gestione classi WMI e metodi per gestire le condivisioni e l'accesso alla condivisione.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server offre opzioni minime di installazione del server per i computer in Windows server 2008 o versione successiva. Windows Server 2012 offre Server Core sia come configurazione che come opzione di installazione.

-   [Windows Server Backup](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    La Windows Backup server consente di eseguire automaticamente il backup e il ripristino dei dati dell'applicazione. Windows Server 2012 include l'API Cloud Backup Provider.

-   [Windows Condivisione desktop](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows Condivisione desktop è una tecnologia di condivisione dello schermo a più parti. Windows Server 2012 implementa questa tecnologia usando l'API Windows duplicazione.

-   [Servizi Desktop remoto](../termserv/terminal-services-portal.md)

    Windows Condivisione desktop consente all'utente di accedere in remoto a un'istanza del sistema operativo. Windows Server 2012 include una serie di nuove funzionalità, tra cui sessioni figlio, RemoteFX reindirizzamento dei supporti e il client Desktop remoto Broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell è una shell della riga di comando basata su attività e un linguaggio di scripting progettato appositamente per l'amministrazione del sistema. Una novità di Windows Server 2012, Windows PowerShell v3 supporta il flusso di lavoro Windows PowerShell, che sfrutta i vantaggi di Windows Workflow Foundation per consentire l'automazione di attività a esecuzione elevata.

-   [OData di gestione](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Novità** Noto anche come Windows PowerShell Web Services, Management OData, una novità di Windows PowerShell v3, consente la creazione di un end point del servizio Web ASP.NET che espone i dati di gestione, acess tramite comandi Windows PowerShell, come entità del servizio Web OData.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Server 2012 R2 su TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 e Windows Server 2012 libreria TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 in Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
