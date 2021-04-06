---
description: Nell'elenco seguente vengono descritte le aree di funzionalità nuove e aggiornate per Windows Server 2012 e Windows Server 2012 R2. Per ulteriori informazioni sulle nuove tecnologie Windows 8 e Windows 8.1, vedere tecnologie Windows 8 e Windows 8.1.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Novità: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883266"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Novità: Windows Server 2012 R2 & Windows Server 2012

Nell'elenco seguente vengono descritte le aree di funzionalità nuove e aggiornate per Windows Server 2012 e Windows Server 2012 R2. Per ulteriori informazioni sulle nuove tecnologie Windows 8 e Windows 8.1, vedere [tecnologie Windows 8 e Windows 8.1](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Novità di Windows Server 2012 R2

-   [Deduplicazione dati](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    La deduplicazione dei dati consente di trovare e rimuovere la duplicazione nei dati di un volume garantendo al tempo stesso la correttezza e il completamento dei dati. In questo modo è possibile memorizzare un maggior quantitativo di dati dei file in meno spazio del volume. Per Windows Server 2012 R2, sono stati attivati un numero di parametri e codici di errore e la classe [**MSFT \_ DedupFileMetadata**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) è stata aggiunta.

-   [Registrazione inventario software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Novità** Registrazione inventario software raccoglie i dati sulle licenze per il software installato in un server Windows e fornisce l'accesso remoto ai dati in modo che possano essere aggregati facilmente da un Data Center.

-   [Server di destinazione iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    L'API server di destinazione iSCSI fornisce provider di Strumentazione gestione Windows (WMI) per la gestione del server di destinazione iSCSI Microsoft, ad esempio la creazione di dischi virtuali e la relativa presentazione al client. Sono state aggiunte alcune nuove funzionalità per Windows Server 2012 R2.

-   [Registrazione della gestione dei dispositivi mobili](../mdmreg/mobile-device-management-registration-portal.md)

    **Novità** Una tendenza al settore è stata sviluppata in cui i dipendenti connettono i propri dispositivi di elaborazione mobile personali alla rete aziendale e alle risorse (in locale o nel cloud) per eseguire attività lavorative. Questa tendenza richiede il supporto per semplificare la configurazione della rete e delle risorse, in modo che i dipendenti possano registrare i dispositivi personali con la società per scopi lavorativi. Le applicazioni e la tecnologia per supportare la configurazione semplificata devono anche consentire ai professionisti IT di gestire i rischi associati alla presenza di dispositivi non controllati connessi alla rete aziendale. La registrazione di gestione di dispositivi mobili (MDM) registra un dispositivo in un servizio di gestione.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell è una shell da riga di comando basata su attività e un linguaggio di scripting progettato appositamente per l'amministrazione del sistema. Una novità di Windows Server 2012 R2, Windows PowerShell V4 supporta desired state Configuration, una nuova piattaforma di gestione di Windows PowerShell che consente di distribuire e gestire i dati di configurazione per i servizi software e di gestire l'ambiente in cui vengono eseguiti questi servizi.

## <a name="whats-new-for-windows-server-2012"></a>Novità di Windows Server 2012

-   [Clustering di Windows](/previous-versions/windows/desktop/mscs/windows-clustering)

    Il servizio cluster di Windows consente di gestire i cluster con bilanciamento del carico di rete e i cluster di failover. In questa versione sono state aggiunte numerose nuove funzionalità, tra cui nuove funzionalità di gestione dei gruppi, proprietà comuni e integrazione con WMI.

-   [Registrazione accesso utenti](/previous-versions/windows/desktop/ual/user-access-logging)

    **Novità** Registrazione accesso utenti (registrazione accesso utenti) è un Framework comune per i ruoli di Windows Server per segnalare le rispettive metriche di consumo. Questo framework registrazione accesso utenti è un componente fondamentale e essenziale della soluzione di gestione delle licenze più ampia.

-   [Gestione remota Windows](../winrm/portal.md)

    Gestione remota Windows (WinRM) è l'implementazione di Microsoft del protocollo WS-Management, un protocollo standard basato su SOAP (Simple Object Access Protocol) adatto al firewall che consente l'interoperabilità di hardware e sistemi operativi di fornitori diversi. Windows Server 2012 include una serie di API di connessione che si concentrano sull'interazione con istanze e Shell in esecuzione.

-   [Infrastruttura di gestione di Windows](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Novità** Le funzionalità di Windows Management Infrastructure (MI) rappresentano la versione più recente delle tecnologie Strumentazione gestione Windows (WMI), basate sullo standard CIM di DMTF (Distributed Management Task Force). MI è completamente compatibile con le versioni precedenti di WMI e offre una serie di funzionalità e vantaggi che semplificano la progettazione e lo sviluppo di provider e client.

-   [Deduplicazione dati](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Novità** La deduplicazione dei dati consente di trovare e rimuovere la duplicazione nei dati di un volume garantendo al tempo stesso la correttezza e il completamento dei dati. In questo modo è possibile memorizzare un maggior quantitativo di dati dei file in meno spazio del volume.

-   [Server di destinazione iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Novità** L'API server di destinazione iSCSI fornisce provider di Strumentazione gestione Windows (WMI) per la gestione del server di destinazione iSCSI Microsoft, ad esempio la creazione di dischi virtuali e la relativa presentazione al client.

-   [Provider NFS per WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Novità** Il provider WMI per NFS fornisce un mezzo per gestire le impostazioni del server e del client NFS, le condivisioni file, netgroup e i gruppi di client.

-   [File offline](../devnotes/offline-files.md)

    L'API File offline consente alle applicazioni di controllare e monitorare il comportamento di File offline a livello di codice. Windows Server 2012 aggiunge le funzioni [**OfflineFilesQueryStatusEx**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**OfflineFilesStart**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) e [**RenameItem**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) .

-   [Gestione SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Novità** L'API di gestione SMB fornisce le classi e i metodi WMI per gestire le condivisioni e l'accesso alla condivisione.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server fornisce opzioni di installazione minime del server per i computer in esecuzione nel sistema operativo Windows Server 2008 o versioni successive. Windows Server 2012 offre Server Core sia come configurazione che come opzioni di installazione.

-   [Windows Server Backup](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    La funzionalità Windows Server Backup esegue automaticamente il backup e il ripristino dei dati dell'applicazione. Windows Server 2012 include l'API del provider di backup cloud.

-   [Condivisione desktop di Windows](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows Desktop Sharing è una tecnologia di condivisione dello schermo a più parti. Windows Server 2012 implementa questa tecnologia usando l'API di duplicazione di Windows.

-   [Servizi Desktop remoto](../termserv/terminal-services-portal.md)

    Condivisione desktop di Windows consente all'utente di accedere in remoto a un'istanza del sistema operativo. Windows Server 2012 include una serie di nuove funzionalità, incluse le sessioni figlio, il reindirizzamento dei supporti RemoteFX e il client di Desktop remoto broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell è una shell da riga di comando basata su attività e un linguaggio di scripting progettato appositamente per l'amministrazione del sistema. Una novità di Windows Server 2012, Windows PowerShell V3 supporta il flusso di lavoro di Windows PowerShell, che sfrutta i vantaggi di Windows Workflow Foundation per consentire l'automazione di attività a esecuzione prolungata.

-   [OData di gestione](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Novità** Noto anche come servizi Web di Windows PowerShell, gestione OData, una novità di Windows PowerShell V3, consente la creazione di un endpoint del servizio Web ASP.NET che espone i dati di gestione, ad esempio i comandi di Windows PowerShell, come entità del servizio Web OData.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Server 2012 R2 su TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 e Windows Server 2012 nella libreria TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 in Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
