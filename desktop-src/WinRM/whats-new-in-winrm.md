---
title: Novità di WinRM 2,0
description: Le nuove funzionalità sono disponibili nella versione Gestione remota Windows 2,0. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398670"
---
# <a name="whats-new-in-winrm-20"></a>Novità di WinRM 2,0

Le nuove funzionalità sono disponibili nella versione Gestione remota Windows 2,0. (WinRM 2,0)

WinRM 2,0 è incluso in Windows Server 2008 R2 e Windows 7.

È inoltre possibile scaricare WinRM 2,0 per Windows Server 2008 con Service Pack 2 (SP2) e Windows Vista con Service Pack 2 (SP2). Per informazioni sul download di WinRM 2,0, vedere [KB968929](https://support.microsoft.com/kb/968929).

La tabella seguente elenca la documentazione per WinRM 2,0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="client-shell-api.md">API shell del client WinRM</a><br/></td>
<td>Il Application Programming Interface della shell client WinRM (API) fornisce funzionalità per la creazione e la gestione di Shell e operazioni Shell, comandi e flussi di dati in computer remoti. <br/></td>
</tr>
<tr class="even">
<td><a href="winrm-plugin-api.md">API del plug-in WinRM</a><br/></td>
<td>L'API del plug-in WinRM fornisce funzionalità che consentono a un utente di scrivere plug-in implementando determinate API per le operazioni e gli <a href="windows-remote-management-glossary.md"><em>URI di risorse</em></a> supportati.<br/></td>
</tr>
<tr class="odd">
<td><a href="winrm-application-hosting.md">Infrastruttura per la gestione dei servizi ospitati</a><br/></td>
<td>WinRM 2,0 introduce un Framework di hosting. Sono supportati due modelli di hosting. Uno è basato su Internet Information Services (IIS) e l'altro è basato su WinRM-servizio. <br/> Per ulteriori informazioni sulla configurazione dell'host, vedere gli argomenti seguenti:<br/>
<ul>
<li><a href="iis-host-plug-in-configuration.md">Configurazione del plug-in host IIS</a></li>
<li><a href="wsman-service-plug-in-configuration.md">Configurazione del plug-in del servizio WinRM</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="dmtf-association-traversal.md">Individuazione del profilo DMTF tramite l'attraversamento dell'associazione</a><br/></td>
<td>L'attraversamento delle associazioni consente a un utente di recuperare le istanze delle classi di associazione usando un meccanismo di filtro standard.<br/></td>
</tr>
<tr class="odd">
<td><a href="remote-shell-infrastructure-improvements.md">Miglioramenti dell'infrastruttura della shell remota</a><br/></td>
<td>Questo argomento include informazioni sui miglioramenti dell'infrastruttura remota per WinRM. <br/></td>
</tr>
<tr class="even">
<td><a href="multi-hop-support.md">Supporto di più hop</a><br/></td>
<td>È stata aggiunta la funzionalità a WinRM 2,0 che supporta la delega delle credenziali utente tra più computer remoti. <br/> L'argomento delle <a href="authentication-constants.md"><strong>costanti di autenticazione</strong></a> è stato aggiornato per aggiungere la costante seguente: <strong>WSManFlagUseCredSsp</strong>.<br/> È stata aggiunta la seguente API C++ per fornire supporto per più hop: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br/> È stata aggiunta l'API di scripting seguente per fornire supporto per più hop: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="quotas.md">Gestione delle quote per le shell remote</a><br/></td>
<td>Questo argomento include informazioni sulla configurazione della quota per la gestione della shell remota.<br/></td>
</tr>
<tr class="even">
<td><a href="winrm-powershell-commandlets.md">Riferimenti gestiti per i comandi di WS-Management PowerShell</a><br/></td>
<td>Gli utenti di WinRM 2,0 possono usare i cmdlet di Windows PowerShell per la gestione del sistema.<br/></td>
</tr>
</tbody>
</table>



 

 

 





