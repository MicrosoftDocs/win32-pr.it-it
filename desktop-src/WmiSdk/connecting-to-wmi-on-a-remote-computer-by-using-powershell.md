---
description: Connessione a WMI in modalità remota con PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Connessione a WMI in modalità remota con PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d499c59ee6774b1e972e192dfc2c0d1228469196c66e8f3feb80d1c9d6339c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679871"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a>Connessione a WMI in modalità remota con PowerShell

Windows PowerShell fornisce un meccanismo semplice per connettersi Windows Management Instrumentation (WMI) in un computer remoto. Le connessioni remote in WMI sono interessate dal firewall [Windows,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))dalle impostazioni DCOM e dal [controllo dell'account utente .](/previous-versions/aa905108(v=msdn.10)) Per altre informazioni sulla configurazione delle connessioni remote, vedere Connessione a WMI in modalità remota a [partire da Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).

Gli esempi in questo argomento sono basati su VBScript di [Connessione a WMI in un computer remoto.](connecting-to-wmi-on-a-remote-computer.md) Tutti gli esempi in questo argomento usano il cmdlet [Get-WmiObject.](/previous-versions//dd315295(v=technet.10)) Per altre informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

## <a name="windows-powershell-examples"></a>Windows PowerShell esempi

Quando si crea una connessione a un computer remoto, un utente può specificare le informazioni di connessione, ad esempio il nome del computer remoto, le credenziali e il livello di autenticazione per la connessione. Gli esempi seguenti illustrano come connettersi a un computer remoto usando diversi set di credenziali e come accedere alle informazioni WMI.

Nell'esempio Windows PowerShell seguente viene illustrata l'impostazione del livello di rappresentazione:


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



Nell'esempio precedente l'utente si connette a un computer remoto usando le stesse credenziali (dominio e nome utente) con cui ha eseguito l'accesso. L'utente ha anche richiesto di usare la rappresentazione. A differenza dell'esempio VBScript originale, non è necessaria una stringa del moniker perché il livello di rappresentazione è impostato dalla proprietà "Impersonation". Per impostazione predefinita, il livello di rappresentazione è impostato su 3 (Rappresenta).

Nell'esempio vengono elencate tutte le istanze della [**classe \_ Processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in esecuzione nel computer remoto.

> [!Note]  
> È necessario specificare lo spazio dei nomi WMI a cui connettersi nel computer remoto perché è possibile che lo spazio dei nomi predefinito non sia lo stesso in computer diversi.

 

L'Windows PowerShell seguente illustra come connettersi a un computer remoto con credenziali diverse e impostare il livello di rappresentazione su 3, ovvero Rappresenta:


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



Nell'esempio precedente il nome del computer è stato assegnato alla variabile $Computer. L'utente si connette a un computer remoto usando credenziali specifiche (dominio e nome utente) e richiede la rappresentazione per il livello di autenticazione.

> [!Note]  
> Il carattere grave accentato ( \` ) viene usato per indicare un'interruzione di riga. Equivale al carattere di sottolineatura ( \_ ) in VBScript.

 

L'esempio Windows PowerShell seguente si connette a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e visualizzando quindi i nomi dei dispositivi Plug and Play, ovvero le istanze di [**Win32 \_ PnPEntity,**](/windows/desktop/CIMWin32Prov/win32-pnpentity)in ogni computer:


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
> Per eseguire lo script di Windows PowerShell precedente, è necessario essere un amministratore nei computer remoti. Inoltre, in relazione all'esempio precedente, tenere presente quanto segue:

 

-   I nomi dei computer nella matrice devono essere racchiusi tra virgolette perché sono stringhe.
-   Gli oggetti restituiti da [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) vengono assegnati alla $ColItems variabile.
-   L'operatore \[ \] range ha limitato l'elenco Plug and Play dispositivi a 48 istanze. Per altre informazioni, vedere [Informazioni sugli \_ operatori](/previous-versions//dd347588(v=technet.10)).
-   " \| " è il carattere della pipeline. L'oggetto restituito da ColItems viene inviato al cmdlet [Format-List.]( /previous-versions//dd347700(v=technet.10))

L'Windows PowerShell seguente consente di connettersi a un computer remoto in un dominio diverso. In questo esempio vengono visualizzati anche i nomi dei processi per le istanze di [**Processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) nel computer remoto.


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
> Per eseguire lo script Windows PowerShell precedente, è necessario essere un amministratore nel computer remoto.

 

Nell'esempio precedente l'utente si connette a un computer remoto in un dominio diverso e specifica le impostazioni locali preferite. Il [comando Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente e le assegna a un oggetto. Nell'esempio vengono inoltre elencati i nomi delle istanze della [**classe Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) in esecuzione nel computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
