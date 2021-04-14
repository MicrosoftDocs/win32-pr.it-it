---
description: La comunicazione con un dispositivo di rete tramite l'interfaccia SNMP WMI richiede la configurazione del dispositivo, SNMP e dei servizi WMI. Le informazioni contenute in questo argomento illustrano come configurare l'ambiente WMI SNMP.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Configurazione dell'ambiente WMI SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349226"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="be916-104">Configurazione dell'ambiente WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="be916-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="be916-105">La comunicazione con un dispositivo di rete tramite l'interfaccia SNMP WMI richiede la configurazione del dispositivo, SNMP e dei servizi WMI.</span><span class="sxs-lookup"><span data-stu-id="be916-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="be916-106">Le informazioni contenute in questo argomento illustrano come configurare l'ambiente WMI SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="be916-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="be916-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="be916-108">Installazione del provider SNMP</span><span class="sxs-lookup"><span data-stu-id="be916-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="be916-109">Il servizio SNMP non è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="be916-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="be916-110">È possibile abilitare il servizio SNMP e il provider SNMP WMI tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="be916-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="be916-111">Tenere presente che il servizio SNMP deve essere abilitato e in esecuzione affinché il provider SNMP WMI funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="be916-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="be916-112">A partire da Windows Vista, utilizzare la procedura seguente per installare il provider SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="be916-113">**Per installare il provider SNMP**</span><span class="sxs-lookup"><span data-stu-id="be916-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="be916-114">Dal **Pannello di controllo**, selezionare **programmi**.</span><span class="sxs-lookup"><span data-stu-id="be916-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="be916-115">In **programmi e funzionalità** fare clic **su attivazione o disattivazione delle funzionalità Windows**.</span><span class="sxs-lookup"><span data-stu-id="be916-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="be916-116">Nell'elenco funzionalità Windows scorrere fino alla **funzionalità SNMP** ed espandere l'elenco in modo che sia possibile visualizzare il **provider SNMP WMI**.</span><span class="sxs-lookup"><span data-stu-id="be916-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="be916-117">Selezionare la casella di controllo **provider SNMP WMI**.</span><span class="sxs-lookup"><span data-stu-id="be916-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="be916-118">La casella di controllo per la **funzionalità SNMP** viene selezionata automaticamente perché il provider richiede SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="be916-119">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="be916-119">Click **OK**.</span></span>
6.  <span data-ttu-id="be916-120">Da un prompt dei comandi o dal menu **Start** , eseguire Services. msc e verificare che il servizio SNMP sia stato avviato.</span><span class="sxs-lookup"><span data-stu-id="be916-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="be916-121">Creazione di uno spazio dei nomi SNMP</span><span class="sxs-lookup"><span data-stu-id="be916-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="be916-122">Uno spazio dei nomi SNMP definisce una visualizzazione di un dispositivo di rete.</span><span class="sxs-lookup"><span data-stu-id="be916-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="be916-123">Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="be916-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="be916-124">Nella procedura riportata di seguito viene descritto come creare uno [*spazio dei nomi*](gloss-n.md)WMI SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="be916-125">**Per creare uno spazio dei nomi SNMP**</span><span class="sxs-lookup"><span data-stu-id="be916-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="be916-126">Creare un'istanza della classe di sistema [**\_ \_ dello spazio dei nomi**](--namespace.md) compilando un file [*Managed Object Format*](gloss-m.md) . mof o utilizzando l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="be916-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="be916-127">Per ulteriori informazioni, vedere [creazione di gerarchie all'interno di WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="be916-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="be916-128">Associare i [*qualificatori*](gloss-q.md) del provider SNMP alla definizione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="be916-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="be916-129">I qualificatori del provider SNMP contengono informazioni sul contesto specifiche dell'implementazione e proprietà del trasporto che definiscono il modo in cui il provider SNMP accede a un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="be916-130">Per ulteriori informazioni, vedere [**qualificatori specifici del provider SNMP**](qualifiers-specific-to-the-snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="be916-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="be916-131">Utilizzare lo strumento da riga di comando [mofcomp](mofcomp.md) per caricare il codice MOF nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="be916-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="be916-132">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="be916-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="be916-133">Nell'esempio di codice MOF seguente viene definito lo \\ spazio dei nomi SNMP con un subset dei qualificatori che possono essere associati a uno spazio dei nomi SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="be916-134">Inserimento di dati MIB SNMP in WMI</span><span class="sxs-lookup"><span data-stu-id="be916-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="be916-135">Come provider, il provider SNMP funge da Bridge tra i dati SNMP e le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="be916-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="be916-136">Pertanto, è necessario disporre di classi in WMI che rappresentano aspetti diversi di un dispositivo abilitato SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="be916-137">A tale scopo, è necessario utilizzare il compilatore[smi2smir](smi2smir.md)(SNMP Information Module) per compilare le informazioni di gestione SNMP dal formato SNMP nelle definizioni dello schema CIM equivalenti.</span><span class="sxs-lookup"><span data-stu-id="be916-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="be916-138">È quindi possibile indirizzare l'output del compilatore di informazioni in un database dello schema SNMP denominato "SNMP Module Information Repository (archivio SMIR)" o a diversi tipi di file MOF.</span><span class="sxs-lookup"><span data-stu-id="be916-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="be916-139">Il compilatore viene eseguito nella modalità da riga di comando, usando un file MIB come input.</span><span class="sxs-lookup"><span data-stu-id="be916-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="be916-140">Il comando seguente carica il file MIB specificato in archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="be916-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="be916-141">\**smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="be916-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="be916-142">Configurazione di community SNMP</span><span class="sxs-lookup"><span data-stu-id="be916-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="be916-143">Come misura di sicurezza, la community SNMP "public" non viene creata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="be916-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="be916-144">È possibile creare la community come descritto in [impostazioni del registro di sistema](/previous-versions/windows/embedded/ms907028(v=msdn.10))per le community.</span><span class="sxs-lookup"><span data-stu-id="be916-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="be916-145">Se non si dispone di community, creare la community "public" per accedere al provider SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="be916-146">Generazione di file MOF da file MIB</span><span class="sxs-lookup"><span data-stu-id="be916-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="be916-147">I comandi seguenti sono un esempio di come generare file MOF dai file MIB installati durante l'installazione del provider SNMP.</span><span class="sxs-lookup"><span data-stu-id="be916-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="be916-148">**CD** *% windir% \\ system32 \\ WBEM \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="be916-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="be916-149">**Smi2smir/g** *.. \\ . \\ hostmib. MIB* **>** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="be916-150">**Smi2smir/g** *.. \\ . \\ ipforwd. MIB* **>** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="be916-151">**Smi2smir/g** *.. \\ . \\ nipx. MIB* **>** *nipx. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="be916-152">**Smi2smir/g** *.. \\ . \\ MIB \_ II. MIB* MIB **>** *\_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="be916-153">**Smi2smir/g** *.. \\ . \\ lmmib2. MIB* **>** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="be916-154">**Smi2smir/g** *.. \\ . \\ mcastmib. MIB* **>** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="be916-155">**Smi2smir/g** *.. \\ . \\ rfc2571. MIB* **>** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="be916-156">**Smi2smir/g** *.. \\ . \\ wfospf. MIB* **>** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="be916-157">**Smi2smir/g** *.. \\ . \\ DHCP. MIB.. \\ . \\ MSFT. MIB* **>** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="be916-158">**Smi2smir/g** *.. \\ . \\ WINS. MIB.. \\ . \\ MSFT. MIB* **>** *WINS. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="be916-159">**Smi2smir/g** *.. \\ . \\ mipx. MIB.. \\ . \\ MSFT. MIB* **>** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="be916-160">**Smi2smir/g** *.. \\ . \\ mripsap. MIB.. \\ . \\ MSFT. MIB* **>** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="be916-161">**Smi2smir/g** *.. \\ . \\ msipbtp. MIB.. \\ . \\ MSFT. MIB* **>** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="be916-162">**Smi2smir/g** *.. \\ . \\ msiprip2. MIB.. \\ . \\ MSFT. MIB* **>** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="be916-163">Aggiunta di file MOF SNMP al repository WMI</span><span class="sxs-lookup"><span data-stu-id="be916-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="be916-164">I comandi seguenti sono un esempio di come aggiungere i file MOF generati dai file MIB al repository WMI.</span><span class="sxs-lookup"><span data-stu-id="be916-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="be916-165">Se si desidera aggiungere i file MOF all'elenco di file da ripristinare automaticamente in un ripristino del [*repository WMI*](gloss-w.md) , aggiungere il flag **-autocover** alla fine di ogni comando.</span><span class="sxs-lookup"><span data-stu-id="be916-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="be916-166">Per ulteriori informazioni su WMI Mofcomp.exe strumento da riga di comando, vedere [**mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="be916-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="be916-167">**mofcomp** *hostmib. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="be916-168">**mofcomp** *ipforwd. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="be916-169">**mofcomp** *nipx. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="be916-170">**mofcomp** *MIB \_ II. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="be916-171">**mofcomp** *lmmib2. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="be916-172">**mofcomp** *mcastmib. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="be916-173">**mofcomp** *rfc2571. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="be916-174">**mofcomp** *wfospf. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="be916-175">**mofcomp** *DHCP. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="be916-176">**mofcomp** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="be916-177">**mofcomp** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="be916-178">**mofcomp** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="be916-179">**mofcomp** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="be916-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="be916-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be916-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be916-181">Accesso ai dispositivi SNMP</span><span class="sxs-lookup"><span data-stu-id="be916-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
