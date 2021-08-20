---
title: Novità di WinRM 2.0
description: Le nuove funzionalità sono disponibili in Windows Gestione remota versione 2.0. (WinRM 2.0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d322b0b86600cd783bd787427b53df334f3d499a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480587"
---
# <a name="whats-new-in-winrm-20"></a>Novità di WinRM 2.0

Le nuove funzionalità sono disponibili in Windows Gestione remota versione 2.0. (WinRM 2.0)

WinRM 2.0 è incluso in Windows Server 2008 R2 e Windows 7.

È anche possibile scaricare WinRM 2.0 per Windows Server 2008 con Service Pack 2 (SP2) e Windows Vista con Service Pack 2 (SP2). Per informazioni sul download di WinRM 2.0, vedere [KB968929](https://support.microsoft.com/kb/968929).

La tabella seguente elenca la documentazione per WinRM 2.0.




| Argomento | Descrizione | 
|-------|-------------|
| <a href="client-shell-api.md">API shell del client WinRM</a><br /> | L'API (Application Programming Interface) di WinRM Client Shell offre funzionalità per creare e gestire shell e operazioni della shell, comandi e flussi di dati nei computer remoti. <br /> | 
| <a href="winrm-plugin-api.md">API plug-in WinRM</a><br /> | L'API plug-in WinRM offre funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per le operazioni e gli <a href="windows-remote-management-glossary.md"><em>URI</em></a> delle risorse supportati.<br /> | 
| <a href="winrm-application-hosting.md">Infrastruttura per la gestione dei servizi ospitati</a><br /> | WinRM 2.0 introduce un framework di hosting. Sono supportati due modelli di hosting. Una è basata su Internet Information Service (IIS) e l'altra è basata sul servizio WinRM. <br /> Per altre informazioni sulla configurazione dell'host, vedere gli argomenti seguenti:<br /><ul><li><a href="iis-host-plug-in-configuration.md">Configurazione del plug-in dell'host IIS</a></li><li><a href="wsman-service-plug-in-configuration.md">Configurazione del plug-in del servizio Gestione remota Windows</a></li></ul> | 
| <a href="dmtf-association-traversal.md">Individuazione profilo DMTF tramite attraversamento associazione</a><br /> | L'attraversamento dell'associazione consente a un utente di recuperare istanze delle classi association usando un meccanismo di filtro standard.<br /> | 
| <a href="remote-shell-infrastructure-improvements.md">Miglioramenti dell'infrastruttura di Remote Shell</a><br /> | Questo argomento include informazioni sui miglioramenti dell'infrastruttura remota per Gestione remota Windows. <br /> | 
| <a href="multi-hop-support.md">Supporto multi hop</a><br /> | È stata aggiunta a WinRM 2.0 la funzionalità che supporta la delega delle credenziali utente in più computer remoti. <br /> <a href="authentication-constants.md"><strong>L'argomento Costanti di</strong></a> autenticazione è stato aggiornato per aggiungere la costante <strong>seguente: WSManFlagUseCredSsp</strong>.<br /> L'API C++ seguente è stata aggiunta per fornire il supporto multi hop: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br /> È stata aggiunta l'API di scripting seguente per fornire il supporto multi hop: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp</strong></a>.<br /> | 
| <a href="quotas.md">Gestione delle quote per le shell remote</a><br /> | Questo argomento include informazioni sulla configurazione della quota per la gestione della shell remota.<br /> | 
| <a href="winrm-powershell-commandlets.md">Informazioni di riferimento gestite WS-Management comandi di PowerShell</a><br /> | Gli utenti di WinRM 2.0 possono usare Windows PowerShell cmdlet per la gestione del sistema.<br /> | 




 

 

 





