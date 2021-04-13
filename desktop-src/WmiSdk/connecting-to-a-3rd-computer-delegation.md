---
description: Quando si esegue uno script in un sistema locale che ottiene dati da un sistema remoto, WMI fornisce le credenziali al provider dei dati nel sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delega con WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401832"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="e79e9-103">Delega con WMI</span><span class="sxs-lookup"><span data-stu-id="e79e9-103">Delegating with WMI</span></span>

<span data-ttu-id="e79e9-104">Quando si esegue uno script in un sistema locale che ottiene dati da un sistema remoto, WMI fornisce le credenziali al provider dei dati nel sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="e79e9-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="e79e9-105">È necessario solo un livello di **rappresentazione, perché** è necessario solo un hop di rete.</span><span class="sxs-lookup"><span data-stu-id="e79e9-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="e79e9-106">Tuttavia, se lo script si connette a WMI nel sistema remoto e tenta di aprire un file di log in un sistema remoto aggiuntivo, lo script avrà esito negativo a meno che il livello di rappresentazione non sia **delegato**.</span><span class="sxs-lookup"><span data-stu-id="e79e9-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="e79e9-107">Il livello di rappresentazione del **delegato** è necessario per qualsiasi operazione che implica più di un hop di rete.</span><span class="sxs-lookup"><span data-stu-id="e79e9-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="e79e9-108">Per ulteriori informazioni sulla sicurezza DCOM in WMI, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="e79e9-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="e79e9-109">Per ulteriori informazioni su una connessione hop a una rete tra due computer, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="e79e9-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="e79e9-110">**Per utilizzare la delega per connettersi a un computer tramite un altro computer**</span><span class="sxs-lookup"><span data-stu-id="e79e9-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="e79e9-111">Abilitare la delega in Active Directory (**Active Directory utenti e computer** nel **Pannello di controllo** **attività amministrative**) sul controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="e79e9-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="e79e9-112">L'account nel sistema remoto deve essere contrassegnato come **trusted per la delega** e l'account nel sistema locale non deve essere contrassegnato come l' **account è sensibile e non può essere delegato**.</span><span class="sxs-lookup"><span data-stu-id="e79e9-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="e79e9-113">il sistema locale, il sistema remoto e il controller di dominio devono essere membri dello stesso dominio o in domini trusted.</span><span class="sxs-lookup"><span data-stu-id="e79e9-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="e79e9-114">**Nota**  L'uso della delega costituisce un rischio per la sicurezza perché fornisce ai processi esterni al controllo diretto la possibilità di usare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="e79e9-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="e79e9-115">Modificare il codice nel modo seguente per indicare che si desidera utilizzare la delega.</span><span class="sxs-lookup"><span data-stu-id="e79e9-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="e79e9-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span><span class="sxs-lookup"><span data-stu-id="e79e9-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="e79e9-117">Impostare il parametro *-Impersonation* sul cmdlet WMI per **delegare**.</span><span class="sxs-lookup"><span data-stu-id="e79e9-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="e79e9-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span><span class="sxs-lookup"><span data-stu-id="e79e9-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="e79e9-119">Impostare il parametro *ImpersonationLevel* su **delegate** nella chiamata a [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) o a **delegate** nella stringa del [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="e79e9-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="e79e9-120">È anche possibile impostare la rappresentazione in un oggetto [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="e79e9-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="e79e9-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="e79e9-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="e79e9-122">Impostare il parametro del livello di rappresentazione sul **\_ delegato RPC C \_ Imp \_ level \_** nella chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="e79e9-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="e79e9-123">Per ulteriori informazioni su quando effettuare queste chiamate, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="e79e9-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="e79e9-124">Per passare l'identità del client ai server COM remoti in C++, impostare il mascheramento nella chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="e79e9-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="e79e9-125">Per altre informazioni, vedere [mascheramento](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="e79e9-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="e79e9-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="e79e9-126">Examples</span></span>

<span data-ttu-id="e79e9-127">Nell'esempio di codice seguente viene illustrata una stringa del moniker che imposta la rappresentazione da **delegare**.</span><span class="sxs-lookup"><span data-stu-id="e79e9-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="e79e9-128">Tenere presente che l'autorità deve essere impostata su Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e79e9-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="e79e9-129">Nell'esempio di codice seguente viene illustrato come impostare la rappresentazione su **delegate** (valore 4) utilizzando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="e79e9-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="e79e9-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e79e9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e79e9-131">Protezione di una connessione WMI remota</span><span class="sxs-lookup"><span data-stu-id="e79e9-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="e79e9-132">Creazione di processi in modalità remota con WMI</span><span class="sxs-lookup"><span data-stu-id="e79e9-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
