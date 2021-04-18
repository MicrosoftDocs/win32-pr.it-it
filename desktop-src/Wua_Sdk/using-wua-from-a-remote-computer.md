---
description: L'API dell'agente di Windows Update (WUA) può essere usata da un utente in un computer remoto o da un'applicazione in esecuzione in un computer remoto. Tuttavia, l'utente remoto o l'applicazione deve disporre di privilegi di amministratore.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Uso di WUA da un computer remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305829"
---
# <a name="using-wua-from-a-remote-computer"></a>Uso di WUA da un computer remoto

L'API dell'agente di Windows Update (WUA) può essere usata da un utente in un computer remoto o da un'applicazione in esecuzione in un computer remoto. Tuttavia, l'utente remoto o l'applicazione deve disporre di privilegi di amministratore.

L'elenco seguente contiene le interfacce disponibili per gli utenti e le applicazioni remote:

-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**ISearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [**IUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [**IUpdateIdentity**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [**IImageInformation**](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [**Tringcollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [**ICategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [**IUpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [**IUpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [**IUpdateDownloadContentCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [**IUpdateDownloadContent**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

L'elenco seguente contiene le interfacce e le proprietà che non sono disponibili per gli utenti e le applicazioni remote:

-   [**IUpdateSession::CreateUpdateDownloader**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [**IUpdateSession::CreateUpdateInstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [**Proprietà WebProxy di IUpdateSession**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   La [**Proprietà IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) **(nascosto** è di sola lettura quando viene chiamata in modalità remota).
-   [**IUpdate:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [**IUpdate:: CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [**IWindowsDriverUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [**IUpdateServiceManager:: AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [**IUpdateServiceManager::RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [**IUpdateServiceManager::UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [**IAutomaticUpdate::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates:: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::ShowSettingsDialog**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [**Proprietà Settings di IAutomaticUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [**Proprietà ServiceEnabled di IAutomaticUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

È necessario aggiungere le seguenti porte ed eccezioni alle impostazioni di Windows Firewall per Windows Vista e Windows Server 2008 affinché l'API WUA venga chiamata in remoto.

<dl> <dt>

<span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Eccezione 1
</dt> <dd> <dl> <dd>Porta locale: 135</dd> <dd>Porta remota: tutti</dd> <dd>Numero di protocollo: 6</dd> <dd>Eseguibile:% windir% \\ system32 \\svchost.exe</dd> <dd>Servizio: RPCSS</dd> <dd>Privilegio remoto: amministratore</dd> </dl> </dd> <dt>

<span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Eccezione 2
</dt> <dd> <dl> <dd>Porta locale: RPC dinamica</dd> <dd>Porta remota: tutti</dd> <dd>Numero di protocollo: 6</dd> <dd>Eseguibile:% windir% \\ system32 \\dllhost.exe</dd> <dd>Privilegio remoto: amministratore</dd> </dl> </dd> </dl>

L'elenco seguente contiene gli strumenti che è possibile usare per configurare le impostazioni di Windows Firewall:

-   Windows Firewall con snap-in Windows Firewall con protezione avanzata
-   Criteri di gruppo
-   Strumento da riga di comando netsh advfirewall

Per ulteriori informazioni su come utilizzare gli strumenti di per configurare le impostazioni di Windows Firewall, vedere [Introduzione con Windows Firewall con sicurezza avanzata](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).

 

 
