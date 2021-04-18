---
description: Nelle sezioni seguenti vengono descritti i problemi comuni che gli sviluppatori possono avere con la creazione di una connessione WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Risoluzione dei problemi relativi a una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309758"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="9ed41-103">Risoluzione dei problemi relativi a una connessione WMI remota</span><span class="sxs-lookup"><span data-stu-id="9ed41-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="9ed41-104">Nelle sezioni seguenti vengono descritti i problemi comuni che gli sviluppatori possono avere con la creazione di una connessione WMI remota.</span><span class="sxs-lookup"><span data-stu-id="9ed41-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="9ed41-105">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="9ed41-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="9ed41-106">Accesso DCOM negato</span><span class="sxs-lookup"><span data-stu-id="9ed41-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="9ed41-107">Errore di connessione</span><span class="sxs-lookup"><span data-stu-id="9ed41-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="9ed41-108">Timeout della connessione WMI</span><span class="sxs-lookup"><span data-stu-id="9ed41-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="9ed41-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ed41-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="9ed41-110">Accesso DCOM negato</span><span class="sxs-lookup"><span data-stu-id="9ed41-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="9ed41-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo</span><span class="sxs-lookup"><span data-stu-id="9ed41-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-112">la connessione non è riuscita con l'errore "accesso DCOM negato", insieme al valore decimale-2147024891 o esadecimale value0x80070005.</span><span class="sxs-lookup"><span data-stu-id="9ed41-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="9ed41-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="9ed41-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-114">DCOM potrebbe non essere configurato per consentire una connessione WMI.</span><span class="sxs-lookup"><span data-stu-id="9ed41-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="9ed41-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione</span><span class="sxs-lookup"><span data-stu-id="9ed41-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-116">È possibile configurare le impostazioni DCOM per WMI utilizzando l'utilità di configurazione DCOM (**DCOMCnfg.exe**) disponibile in **strumenti di amministrazione** nel **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="9ed41-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="9ed41-117">Questa utilità espone le impostazioni che consentono a determinati utenti di connettersi al computer in modalità remota tramite DCOM.</span><span class="sxs-lookup"><span data-stu-id="9ed41-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="9ed41-118">Per impostazione predefinita, i membri del gruppo Administrators possono connettersi in remoto al computer.</span><span class="sxs-lookup"><span data-stu-id="9ed41-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="9ed41-119">Con questa utilità è possibile impostare la sicurezza per l'avvio, l'accesso e la configurazione del servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="9ed41-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="9ed41-120">Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9ed41-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="9ed41-121">Errore di connessione</span><span class="sxs-lookup"><span data-stu-id="9ed41-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="9ed41-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo</span><span class="sxs-lookup"><span data-stu-id="9ed41-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-123">Non è possibile connettersi a WMI in un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="9ed41-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="9ed41-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="9ed41-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-125">È possibile che si stia tentando di connettersi a un sistema che non supporta WMI.</span><span class="sxs-lookup"><span data-stu-id="9ed41-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="9ed41-126">Le seguenti connessioni tra le versioni del sistema operativo non sono supportate:</span><span class="sxs-lookup"><span data-stu-id="9ed41-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="9ed41-127">Non è possibile connettersi a un computer che esegue un'edizione iniziale, di base o Home.</span><span class="sxs-lookup"><span data-stu-id="9ed41-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="9ed41-128">In alternativa, è possibile che si stia tentando di connettersi a uno spazio dei nomi che richiede una connessione crittografata, una che richiede un livello di autenticazione `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** o la **\_ \_ \_ \_ \_ privacy PKT del livello di autenticazione RPC C**.</span><span class="sxs-lookup"><span data-stu-id="9ed41-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="9ed41-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione</span><span class="sxs-lookup"><span data-stu-id="9ed41-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-130">Per ulteriori informazioni, vedere [protezione di spazi dei nomi WMI](securing-wmi-namespaces.md), [protezione di client e provider C++](securing-c---clients-and-providers.md)o [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="9ed41-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="9ed41-131">Timeout della connessione WMI</span><span class="sxs-lookup"><span data-stu-id="9ed41-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="9ed41-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo</span><span class="sxs-lookup"><span data-stu-id="9ed41-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-133">Si verifica il timeout della connessione WMI.</span><span class="sxs-lookup"><span data-stu-id="9ed41-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="9ed41-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="9ed41-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-135">A causa di problemi di ritardo di rete, il computer non è in grado di rispondere nel tempo.</span><span class="sxs-lookup"><span data-stu-id="9ed41-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="9ed41-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione</span><span class="sxs-lookup"><span data-stu-id="9ed41-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="9ed41-137">Quando si esegue la connessione a WMI tramite una chiamata a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), è possibile impostare il flag **wbemConnectFlagUseMaxWait** (scripting) o il **\_ flag WBEM Connect usare il valore \_ \_ \_ Max \_ wait** in C++ su 128 (0x80) per imporre un intervallo di due (2) minuti per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="9ed41-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9ed41-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ed41-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ed41-139">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="9ed41-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



