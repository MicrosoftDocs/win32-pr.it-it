---
description: Connessione a WMI in modalità remota con PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Connessione a WMI in modalità remota con PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755351"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Connessione a WMI in modalità remota con PowerShell

Windows PowerShell fornisce un meccanismo semplice per connettersi a Strumentazione gestione Windows (WMI) in un computer remoto. Le connessioni remote in WMI sono interessate dalla [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), dalle impostazioni DCOM e dal [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)). Per ulteriori informazioni sulla configurazione delle connessioni remote, vedere [connessione a WMI in modalità remota a partire da Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Gli esempi in questo argomento si basano sulla [connessione di VBScript a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md). Tutti gli esempi in questo argomento usano il cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) . Per ulteriori informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>Esempi di Windows PowerShell

Quando si crea una connessione a un computer remoto, un utente può specificare le informazioni di connessione, ad esempio il nome del computer remoto, le credenziali e il livello di autenticazione per la connessione. Negli esempi seguenti viene illustrato come connettersi a un computer remoto utilizzando diversi set di credenziali e come accedere alle informazioni di WMI.

Nell'esempio di Windows PowerShell riportato di seguito viene illustrato come impostare il livello di rappresentazione:


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



Nell'esempio precedente, l'utente si connette a un computer remoto usando le stesse credenziali (dominio e nome utente) con cui è stato effettuato l'accesso. L'utente ha inoltre richiesto di utilizzare la rappresentazione. A differenza dell'esempio VBScript originale, non è necessaria una stringa del moniker perché il livello di rappresentazione è impostato dalla proprietà "rappresentazione". Per impostazione predefinita, il livello di rappresentazione è impostato su 3 (rappresentazione).

Nell'esempio vengono elencate tutte le istanze della classe di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in esecuzione nel computer remoto.

> [!Note]  
> È necessario specificare lo spazio dei nomi WMI a cui connettersi nel computer remoto perché è possibile che lo spazio dei nomi predefinito non sia lo stesso in computer diversi.

 

Nell'esempio di Windows PowerShell riportato di seguito viene illustrato come connettersi a un computer remoto con credenziali diverse e come impostare il livello di rappresentazione su 3, ovvero la rappresentazione:


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



Nell'esempio precedente, il nome del computer è stato assegnato alla variabile $Computer. L'utente si connette a un computer remoto utilizzando credenziali specifiche (dominio e nome utente) e richiede la rappresentazione per il livello di autenticazione.

> [!Note]  
> Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga. Equivale al carattere di sottolineatura ( \_ ) in VBScript.

 

Il seguente esempio di Windows PowerShell si connette a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e quindi visualizzando i nomi dei dispositivi Plug and Play, ovvero le istanze di [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity), in ogni computer:


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> Per eseguire lo script di Windows PowerShell precedente, è necessario essere un amministratore dei computer remoti. Inoltre, in relazione all'esempio precedente, tenere presente quanto segue:

 

-   I nomi di computer nella matrice devono essere racchiusi tra virgolette perché sono stringhe.
-   Gli oggetti restituiti da [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) vengono assegnati alla variabile $ColItems.
-   L'operatore Range \[ \] limita l'elenco di dispositivi Plug and Play a 48 istanze. Per ulteriori informazioni, vedere [About \_ Operators](/previous-versions//dd347588(v=technet.10)).
-   " \| " È il carattere della pipeline. L'oggetto restituito da ColItems viene inviato al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) .

Il seguente esempio di Windows PowerShell consente di connettersi a un computer remoto in un dominio diverso. Questo esempio mostra anche i nomi dei processi per le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) nel computer remoto.


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> Per eseguire lo script di Windows PowerShell precedente, è necessario essere un amministratore nel computer remoto.

 

Nell'esempio precedente, l'utente si connette a un computer remoto in un dominio diverso e specifica le impostazioni locali preferite. Il comando [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente e assegna le credenziali a un oggetto. Nell'esempio vengono inoltre elencati i nomi delle istanze della classe di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in esecuzione nel computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
