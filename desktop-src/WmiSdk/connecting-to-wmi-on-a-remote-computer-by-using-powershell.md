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
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="cb72f-103">Connessione a WMI in modalità remota con PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb72f-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="cb72f-104">Windows PowerShell fornisce un meccanismo semplice per connettersi a Strumentazione gestione Windows (WMI) in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="cb72f-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="cb72f-105">Le connessioni remote in WMI sono interessate dalla [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), dalle impostazioni DCOM e dal [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="cb72f-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="cb72f-106">Per ulteriori informazioni sulla configurazione delle connessioni remote, vedere [connessione a WMI in modalità remota a partire da Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="cb72f-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="cb72f-107">Gli esempi in questo argomento si basano sulla [connessione di VBScript a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="cb72f-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="cb72f-108">Tutti gli esempi in questo argomento usano il cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="cb72f-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="cb72f-109">Per ulteriori informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="cb72f-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="cb72f-110">Esempi di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb72f-110">Windows PowerShell examples</span></span>

<span data-ttu-id="cb72f-111">Quando si crea una connessione a un computer remoto, un utente può specificare le informazioni di connessione, ad esempio il nome del computer remoto, le credenziali e il livello di autenticazione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="cb72f-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="cb72f-112">Negli esempi seguenti viene illustrato come connettersi a un computer remoto utilizzando diversi set di credenziali e come accedere alle informazioni di WMI.</span><span class="sxs-lookup"><span data-stu-id="cb72f-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="cb72f-113">Nell'esempio di Windows PowerShell riportato di seguito viene illustrato come impostare il livello di rappresentazione:</span><span class="sxs-lookup"><span data-stu-id="cb72f-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="cb72f-114">Nell'esempio precedente, l'utente si connette a un computer remoto usando le stesse credenziali (dominio e nome utente) con cui è stato effettuato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="cb72f-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="cb72f-115">L'utente ha inoltre richiesto di utilizzare la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="cb72f-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="cb72f-116">A differenza dell'esempio VBScript originale, non è necessaria una stringa del moniker perché il livello di rappresentazione è impostato dalla proprietà "rappresentazione".</span><span class="sxs-lookup"><span data-stu-id="cb72f-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="cb72f-117">Per impostazione predefinita, il livello di rappresentazione è impostato su 3 (rappresentazione).</span><span class="sxs-lookup"><span data-stu-id="cb72f-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="cb72f-118">Nell'esempio vengono elencate tutte le istanze della classe di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in esecuzione nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="cb72f-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="cb72f-119">È necessario specificare lo spazio dei nomi WMI a cui connettersi nel computer remoto perché è possibile che lo spazio dei nomi predefinito non sia lo stesso in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="cb72f-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="cb72f-120">Nell'esempio di Windows PowerShell riportato di seguito viene illustrato come connettersi a un computer remoto con credenziali diverse e come impostare il livello di rappresentazione su 3, ovvero la rappresentazione:</span><span class="sxs-lookup"><span data-stu-id="cb72f-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="cb72f-121">Nell'esempio precedente, il nome del computer è stato assegnato alla variabile $Computer.</span><span class="sxs-lookup"><span data-stu-id="cb72f-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="cb72f-122">L'utente si connette a un computer remoto utilizzando credenziali specifiche (dominio e nome utente) e richiede la rappresentazione per il livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="cb72f-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="cb72f-123">Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="cb72f-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="cb72f-124">Equivale al carattere di sottolineatura ( \_ ) in VBScript.</span><span class="sxs-lookup"><span data-stu-id="cb72f-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="cb72f-125">Il seguente esempio di Windows PowerShell si connette a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e quindi visualizzando i nomi dei dispositivi Plug and Play, ovvero le istanze di [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity), in ogni computer:</span><span class="sxs-lookup"><span data-stu-id="cb72f-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


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
> <span data-ttu-id="cb72f-126">Per eseguire lo script di Windows PowerShell precedente, è necessario essere un amministratore dei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="cb72f-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="cb72f-127">Inoltre, in relazione all'esempio precedente, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="cb72f-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="cb72f-128">I nomi di computer nella matrice devono essere racchiusi tra virgolette perché sono stringhe.</span><span class="sxs-lookup"><span data-stu-id="cb72f-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="cb72f-129">Gli oggetti restituiti da [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) vengono assegnati alla variabile $ColItems.</span><span class="sxs-lookup"><span data-stu-id="cb72f-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="cb72f-130">L'operatore Range \[ \] limita l'elenco di dispositivi Plug and Play a 48 istanze.</span><span class="sxs-lookup"><span data-stu-id="cb72f-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="cb72f-131">Per ulteriori informazioni, vedere [About \_ Operators](/previous-versions//dd347588(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="cb72f-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="cb72f-132">" \| " È il carattere della pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb72f-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="cb72f-133">L'oggetto restituito da ColItems viene inviato al cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="cb72f-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="cb72f-134">Il seguente esempio di Windows PowerShell consente di connettersi a un computer remoto in un dominio diverso.</span><span class="sxs-lookup"><span data-stu-id="cb72f-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="cb72f-135">Questo esempio mostra anche i nomi dei processi per le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="cb72f-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


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
> <span data-ttu-id="cb72f-136">Per eseguire lo script di Windows PowerShell precedente, è necessario essere un amministratore nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="cb72f-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="cb72f-137">Nell'esempio precedente, l'utente si connette a un computer remoto in un dominio diverso e specifica le impostazioni locali preferite.</span><span class="sxs-lookup"><span data-stu-id="cb72f-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="cb72f-138">Il comando [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente e assegna le credenziali a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb72f-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="cb72f-139">Nell'esempio vengono inoltre elencati i nomi delle istanze della classe di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="cb72f-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb72f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb72f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb72f-141">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="cb72f-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
