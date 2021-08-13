---
title: Riferimento gestito per classi di comandi Windows PowerShell WinRM
description: Windows Gestione remota 2.0 (WinRM) può usare Windows PowerShell cmdlet per la gestione del sistema. Windows PowerShell cmdlet consentono a un amministratore di configurare WinRM e di ottenere dati o gestire le risorse.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- ConnectWSManCommand
- DisableWSManCredSSPCommand
- DisconnectWSManCommand
- EnableWSManCredSSPCommand
- GetWSManCredSSPCommand
- GetWSManInstanceCommand
- InvokeWSManActionCommand
- NewWSManInstanceCommand
- NewWSManSessionOptionCommand
- RemoveWSManInstanceCommand
- SetWSManInstanceCommand
- SetWSManQuickConfigCommand
- TestWSManCommand
- Sessionoption
- AutenticazioneMeccanismo
- ProxyAccessType
- ProxyAuthentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d20a7615be5180350153596502386c9eac7c0c6820442284a717161ee1283e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412451"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Riferimento gestito per classi di comandi Windows PowerShell WinRM

Windows Gestione remota 2.0 (WinRM) può usare Windows PowerShell cmdlet per la gestione del sistema. Windows PowerShell cmdlet consentono a un amministratore di configurare WinRM e di ottenere dati o gestire le risorse.

Windows PowerShell cmdlet per WinRM offrono la stessa funzionalità dell'utilità della riga di comando winrm. Tuttavia, Windows PowerShell esegue anche le operazioni seguenti:

-   Automatizza le attività WinRM in un linguaggio di scripting estendibile e orientato alla gestione.
-   Fornisce un singolo strumento per tutte le attività di gestione.

Vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) per altre informazioni.

## <a name="ws-management-windows-powershell-classes"></a>classi WS-Management Windows PowerShell

**Spazio dei** nomi: Microsoft.WsMan.Management

**Assembly:** System.Management.Automation

Le classi di comando WinRM seguenti vengono implementate da Windows PowerShell. Queste classi sono incluse in questo Sdk (Software Development Kit) solo per completezza. I membri di queste classi non possono essere usati direttamente né devono essere usati per derivare altre classi.



| Classe                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConnectWSManCommand          | Stabilisce la connessione al servizio Gestione remota Windows su un computer remoto. <br/> Vedere il cmdlet [Connessione-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) per esempi e informazioni dettagliate sui parametri.<br/>                                                                                                                                                                                                                                                                                                                                              |
| DisableWSManCredSSPCommand   | Disabilita l'autenticazione CredSSP in un client.<br/> Vedere il cmdlet [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) per informazioni dettagliate sui parametri e per esempi.<br/>                                                                                                                                                                                                                                                                                                                                           |
| DisconnectWSManCommand       | Si disconnette dal servizio Gestione remota Windows in un computer remoto. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Disconnect-WSMan.](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                      |
| EnableWSManCredSSPCommand    | Abilita l'autenticazione CredSSP nel client.<br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Enable-WSManCredSSP.](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                               |
| GetWSManCredSSPCommand       | Ottiene la configurazione correlata a CredSSP per il client.<br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Get-WSManCredSSP.](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                         |
| GetWSManInstanceCommand      | Visualizza le informazioni di gestione per un'istanza di risorsa specificata da un URI di risorsa.<br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Get-WSManInstance.](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                          |
| InvokeWSManActionCommand     | Richiama un'azione sull'oggetto di destinazione specificato dall'URI della risorsa e dai selettori. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Invoke-WSManAction.](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                         |
| NewWSManInstanceCommand      | Crea una nuova istanza di una risorsa di gestione. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [New-WSManInstance.](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                             |
| NewWSManSessionOptionCommand | Crea una tabella hash dell'opzione di sessione WinRM da usare come parametri di input per i cmdlet [WSMan seguenti: Get-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true), [Set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true), [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) [e Connessione-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true). <br/> Per esempi e informazioni dettagliate sui parametri, vedere [New-WSManSessionOption.](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true)<br/> |
| RemoveWSManInstanceCommand   | Elimina un'istanza di risorsa di gestione. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Remove-WSManInstance.](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                                   |
| SetWSManInstanceCommand      | Modifica le informazioni di gestione correlate a una risorsa. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Set-WSManInstance.](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                       |
| SetWSManQuickConfigCommand   | Configura il computer locale per la gestione remota. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Set-WSManQuickConfig.](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                      |
| TestWSManCommand             | Verifica se il servizio Gestione remota Windows è in esecuzione in un computer locale o remoto. <br/> Per esempi e informazioni dettagliate sui parametri, vedere il cmdlet [Test-WSMan.]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                        |
| Sessionoption                | Definisce un set di opzioni estese per la sessione di WS-Management.<br/> Vedere il cmdlet [Connessione-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) per esempi e informazioni dettagliate sui valori possibili.<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>enumerazioni WS-Management Windows PowerShell

Le enumerazioni seguenti vengono implementate da Windows PowerShell. Queste enumerazioni sono incluse in questo Sdk (Software Development Kit) solo per completezza.



| Enumerazione             | Descrizione                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutenticazioneMeccanismo | Specifica il meccanismo di autenticazione da utilizzare nel server. <br/> Vedere il cmdlet [Connessione-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) per esempi e informazioni dettagliate sui valori possibili.<br/>      |
| ProxyAccessType         | Specifica il meccanismo mediante il quale si trova il server proxy.<br/> Per esempi e informazioni dettagliate sui valori possibili, vedere il cmdlet [New-WSManSessionOption.](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true)<br/> |
| ProxyAuthentication     | Specifica il metodo di autenticazione da usare nel proxy.<br/> Per esempi e informazioni dettagliate sui valori possibili, vedere il cmdlet [New-WSManSessionOption.](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true)<br/>      |



 

 

