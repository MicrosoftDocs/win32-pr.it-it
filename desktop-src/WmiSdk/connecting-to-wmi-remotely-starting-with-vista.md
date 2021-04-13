---
description: Per la connessione a uno spazio dei nomi WMI in un computer remoto potrebbe essere necessario modificare le impostazioni di Windows Firewall, controllo dell'account utente (UAC), DCOM o Common Information Model Object Manager (CIMOM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configurazione di una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528615"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="61cfa-103">Configurazione di una connessione WMI remota</span><span class="sxs-lookup"><span data-stu-id="61cfa-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="61cfa-104">Per la connessione a uno spazio dei nomi WMI in un computer remoto potrebbe essere necessario modificare le impostazioni di [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM o Common Information Model Object Manager (CIMOM).</span><span class="sxs-lookup"><span data-stu-id="61cfa-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="61cfa-105">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="61cfa-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="61cfa-106">Impostazioni Windows Firewall</span><span class="sxs-lookup"><span data-stu-id="61cfa-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="61cfa-107">Impostazioni di Controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="61cfa-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="61cfa-108">Impostazioni DCOM</span><span class="sxs-lookup"><span data-stu-id="61cfa-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="61cfa-109">Impostazioni CIMOM</span><span class="sxs-lookup"><span data-stu-id="61cfa-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="61cfa-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61cfa-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="61cfa-111">Impostazioni di Windows Firewall</span><span class="sxs-lookup"><span data-stu-id="61cfa-111">Windows Firewall Settings</span></span>

<span data-ttu-id="61cfa-112">Le impostazioni WMI per Windows Firewall impostazioni abilitano solo le connessioni WMI, anziché altre applicazioni DCOM.</span><span class="sxs-lookup"><span data-stu-id="61cfa-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="61cfa-113">È necessario impostare un'eccezione nel firewall per WMI nel computer di destinazione remoto.</span><span class="sxs-lookup"><span data-stu-id="61cfa-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="61cfa-114">L'eccezione per WMI consente a WMI di ricevere connessioni remote e callback asincroni per Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="61cfa-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="61cfa-115">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="61cfa-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="61cfa-116">Se un'applicazione client crea un sink personalizzato, è necessario aggiungerlo esplicitamente alle eccezioni del firewall per consentire la riuscita dei callback.</span><span class="sxs-lookup"><span data-stu-id="61cfa-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="61cfa-117">L'eccezione per WMI funziona anche se WMI è stato avviato con una porta fissa, usando il comando **winmgmt/standalonehost** .</span><span class="sxs-lookup"><span data-stu-id="61cfa-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="61cfa-118">Per ulteriori informazioni, vedere [configurazione di una porta fissa per WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="61cfa-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="61cfa-119">È possibile abilitare o disabilitare il traffico WMI tramite l'interfaccia utente di Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="61cfa-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="61cfa-120">**Per abilitare o disabilitare il traffico WMI mediante l'interfaccia utente del firewall**</span><span class="sxs-lookup"><span data-stu-id="61cfa-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="61cfa-121">Nel **Pannello di controllo** fare clic su **sicurezza** e quindi su **Windows Firewall**.</span><span class="sxs-lookup"><span data-stu-id="61cfa-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="61cfa-122">Fare clic su **Cambia impostazioni** , quindi fare clic sulla scheda **eccezioni** .</span><span class="sxs-lookup"><span data-stu-id="61cfa-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="61cfa-123">Nella finestra eccezioni selezionare la casella di controllo **Strumentazione gestione Windows (WMI)** per abilitare il traffico WMI attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="61cfa-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="61cfa-124">Per disabilitare il traffico WMI, deselezionare la casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="61cfa-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="61cfa-125">È possibile abilitare o disabilitare il traffico WMI attraverso il firewall al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="61cfa-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="61cfa-126">**Per abilitare o disabilitare il traffico WMI al prompt dei comandi utilizzando il gruppo di regole WMI**</span><span class="sxs-lookup"><span data-stu-id="61cfa-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="61cfa-127">Usare i comandi seguenti al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="61cfa-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="61cfa-128">Digitare quanto segue per abilitare il traffico WMI attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="61cfa-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="61cfa-129">**netsh advfirewall firewall set Rule Group = "Strumentazione gestione Windows (WMI)" nuovo enable = Yes**</span><span class="sxs-lookup"><span data-stu-id="61cfa-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="61cfa-130">Digitare il comando seguente per disabilitare il traffico WMI attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="61cfa-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="61cfa-131">**netsh advfirewall firewall set Rule Group = "Strumentazione gestione Windows (WMI)" nuovo Enable = no**</span><span class="sxs-lookup"><span data-stu-id="61cfa-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="61cfa-132">Anziché utilizzare il singolo comando del gruppo di regole WMI, è possibile utilizzare i singoli comandi per ogni DCOM, servizio WMI e sink.</span><span class="sxs-lookup"><span data-stu-id="61cfa-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="61cfa-133">**Per abilitare il traffico WMI con regole separate per DCOM, WMI, il sink di callback e le connessioni in uscita**</span><span class="sxs-lookup"><span data-stu-id="61cfa-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="61cfa-134">Per stabilire un'eccezione del firewall per la porta DCOM 135, usare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="61cfa-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="61cfa-135">**netsh advfirewall firewall add rule dir = in Name = "DCOM" Program =% SystemRoot% \\ system32 \\svchost.exe Service = RPCSS action = allow Protocol = TCP LocalPort = 135**</span><span class="sxs-lookup"><span data-stu-id="61cfa-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="61cfa-136">Per stabilire un'eccezione del firewall per il servizio WMI, utilizzare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="61cfa-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="61cfa-137">**netsh advfirewall firewall add rule dir = in Name = "WMI" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt action = allow Protocol = TCP LocalPort = any**</span><span class="sxs-lookup"><span data-stu-id="61cfa-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="61cfa-138">Per stabilire un'eccezione del firewall per il sink che riceve i callback da un computer remoto, usare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="61cfa-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="61cfa-139">**netsh advfirewall firewall add rule dir = in Name = "UnsecApp" Program =% SystemRoot% \\ system32 \\ WBEM \\unsecapp.exe action = allow**</span><span class="sxs-lookup"><span data-stu-id="61cfa-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="61cfa-140">Per stabilire un'eccezione del firewall per le connessioni in uscita a un computer remoto con cui il computer locale comunica in modo asincrono, utilizzare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="61cfa-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="61cfa-141">**netsh advfirewall firewall add rule dir = out Name = "WMI \_ out" Program =% SystemRoot% \\ system32 \\svchost.exe Service = WinMgmt action = allow Protocol = TCP LocalPort = any**</span><span class="sxs-lookup"><span data-stu-id="61cfa-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="61cfa-142">Per disabilitare le eccezioni del firewall separatamente, usare i comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="61cfa-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="61cfa-143">**Per disabilitare il traffico WMI con regole separate per DCOM, WMI, il sink di callback e le connessioni in uscita**</span><span class="sxs-lookup"><span data-stu-id="61cfa-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="61cfa-144">Per disabilitare l'eccezione DCOM.</span><span class="sxs-lookup"><span data-stu-id="61cfa-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="61cfa-145">**netsh advfirewall firewall delete rule name = "DCOM"**</span><span class="sxs-lookup"><span data-stu-id="61cfa-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="61cfa-146">Per disabilitare l'eccezione del servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="61cfa-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="61cfa-147">**netsh advfirewall firewall delete rule name = "WMI"**</span><span class="sxs-lookup"><span data-stu-id="61cfa-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="61cfa-148">Per disabilitare l'eccezione del sink.</span><span class="sxs-lookup"><span data-stu-id="61cfa-148">To disable the sink exception.</span></span>

    <span data-ttu-id="61cfa-149">**netsh advfirewall firewall delete rule name = "UnsecApp"**</span><span class="sxs-lookup"><span data-stu-id="61cfa-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="61cfa-150">Per disabilitare l'eccezione in uscita.</span><span class="sxs-lookup"><span data-stu-id="61cfa-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="61cfa-151">**netsh advfirewall firewall delete rule name = "WMI \_ out"**</span><span class="sxs-lookup"><span data-stu-id="61cfa-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="61cfa-152">Impostazioni di Controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="61cfa-152">User Account Control Settings</span></span>

<span data-ttu-id="61cfa-153">Controllo dell'account utente (UAC) l'applicazione di filtri ai token può influire sulle operazioni consentite negli spazi dei nomi WMI o sui dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="61cfa-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="61cfa-154">In controllo dell'account utente, tutti gli account nel gruppo Administrators locale vengono eseguiti con un [*token di accesso*](/windows/desktop/SecGloss/a-gly)utente standard, noto anche come filtro di accesso del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="61cfa-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="61cfa-155">Un account amministratore può eseguire uno script con privilegi elevati, ovvero "Esegui come amministratore".</span><span class="sxs-lookup"><span data-stu-id="61cfa-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="61cfa-156">Quando non ci si connette all'account Administrator predefinito, il controllo dell'account utente influiscono sulle connessioni a un computer remoto in modo diverso a seconda che i due computer si trovino in un dominio o in un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61cfa-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="61cfa-157">Per ulteriori informazioni su UAC e connessioni remote, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="61cfa-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="61cfa-158">Impostazioni DCOM</span><span class="sxs-lookup"><span data-stu-id="61cfa-158">DCOM Settings</span></span>

<span data-ttu-id="61cfa-159">Per ulteriori informazioni sulle impostazioni DCOM, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="61cfa-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="61cfa-160">Tuttavia, UAC influiscono sulle connessioni per gli account utente non di dominio.</span><span class="sxs-lookup"><span data-stu-id="61cfa-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="61cfa-161">Se ci si connette a un computer remoto usando un account utente non di dominio incluso nel gruppo Administrators locale del computer remoto, è necessario concedere in modo esplicito l'accesso DCOM remoto, l'attivazione e i diritti di avvio per l'account.</span><span class="sxs-lookup"><span data-stu-id="61cfa-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="61cfa-162">Impostazioni CIMOM</span><span class="sxs-lookup"><span data-stu-id="61cfa-162">CIMOM Settings</span></span>

<span data-ttu-id="61cfa-163">Se la connessione remota è tra computer che non hanno una relazione di trust, è necessario aggiornare le impostazioni CIMOM. in caso contrario, la connessione asincrona avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="61cfa-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="61cfa-164">Questa impostazione non deve essere modificata per i computer nello stesso dominio o in domini trusted.</span><span class="sxs-lookup"><span data-stu-id="61cfa-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="61cfa-165">La seguente voce del registro di sistema deve essere modificata per consentire callback anonimi:</span><span class="sxs-lookup"><span data-stu-id="61cfa-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="61cfa-166">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**</span><span class="sxs-lookup"><span data-stu-id="61cfa-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="61cfa-167">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="61cfa-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="61cfa-168">Se il valore **AllowAnonymousCallback** è impostato su 0, il servizio WMI impedisce i callback anonimi al client.</span><span class="sxs-lookup"><span data-stu-id="61cfa-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="61cfa-169">Se il valore è impostato su 1, il servizio WMI consente callback anonimi al client.</span><span class="sxs-lookup"><span data-stu-id="61cfa-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61cfa-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61cfa-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61cfa-171">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="61cfa-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
