---
title: BITS Compact Server
description: Il server di Servizio trasferimento intelligente in background (BITS) Compact è un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872753"
---
# <a name="bits-compact-server"></a><span data-ttu-id="322a0-103">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="322a0-103">BITS Compact Server</span></span>

<span data-ttu-id="322a0-104">Il server di Servizio trasferimento intelligente in background (BITS) Compact è un file server HTTP/HTTPS autonomo che consente di trasferire in modo asincrono un numero limitato di file di grandi dimensioni tra computer.</span><span class="sxs-lookup"><span data-stu-id="322a0-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="322a0-105">Compact Server è compilato come servizio NT e utilizza HTTP.SYS.</span><span class="sxs-lookup"><span data-stu-id="322a0-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="322a0-106">BITS Compact Server è progettato per l'uso da parte dei clienti aziendali e Small Business in base alle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="322a0-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="322a0-107">L'utilizzo previsto è costituito da un massimo di 25 gruppi di URL e ogni gruppo di URL supporta 3 trasferimenti di file simultanei.</span><span class="sxs-lookup"><span data-stu-id="322a0-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="322a0-108">I trasferimenti di file si verificano tra computer nello stesso dominio o domini con trust reciproco.</span><span class="sxs-lookup"><span data-stu-id="322a0-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="322a0-109">I trasferimenti di file non sono destinati ai client connessi a Internet.</span><span class="sxs-lookup"><span data-stu-id="322a0-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="322a0-110">Installazione di BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="322a0-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="322a0-111">BITS Compact Server è un componente server facoltativo.</span><span class="sxs-lookup"><span data-stu-id="322a0-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="322a0-112">Per installare BITS Compact Server è possibile usare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="322a0-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="322a0-113">Server Manager</span><span class="sxs-lookup"><span data-stu-id="322a0-113">Server Manager</span></span>

-   <span data-ttu-id="322a0-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="322a0-114">Windows PowerShell</span></span>

-   <span data-ttu-id="322a0-115">Gestione pacchetti</span><span class="sxs-lookup"><span data-stu-id="322a0-115">Package Manager</span></span>

<span data-ttu-id="322a0-116">**Per installare BITS Compact Server utilizzando Server Manager**</span><span class="sxs-lookup"><span data-stu-id="322a0-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="322a0-117">Nella sezione **Riepilogo funzionalità** della **Server Manager** fare clic su **Aggiungi funzionalità**.</span><span class="sxs-lookup"><span data-stu-id="322a0-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="322a0-118">Nell'aggiunta guidata funzionalità selezionare **servizio trasferimento intelligente in background (BITS)** e **Compact Server**.</span><span class="sxs-lookup"><span data-stu-id="322a0-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="322a0-119">Seguire le istruzioni della procedura guidata, inclusa l'installazione del software richiesto, se specificato.</span><span class="sxs-lookup"><span data-stu-id="322a0-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="322a0-120">Per ulteriori informazioni, vedere la Guida in linea di **Server Manager** .</span><span class="sxs-lookup"><span data-stu-id="322a0-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="322a0-121">**Per installare BITS Compact Server usando Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="322a0-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="322a0-122">Al prompt dei comandi di Windows PowerShell digitare il comando seguente: **Import-Module ServerManager**.</span><span class="sxs-lookup"><span data-stu-id="322a0-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="322a0-123">Premere quindi INVIO.</span><span class="sxs-lookup"><span data-stu-id="322a0-123">Then press Enter.</span></span>
2.  <span data-ttu-id="322a0-124">Digitare il comando seguente: **Add-WINDOWSFEATURE BITS-Compact-Server**.</span><span class="sxs-lookup"><span data-stu-id="322a0-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="322a0-125">Premere quindi INVIO.</span><span class="sxs-lookup"><span data-stu-id="322a0-125">Then press Enter.</span></span>

<span data-ttu-id="322a0-126">Nell'esempio basato su testo seguente viene illustrata l'installazione di BITS Compact Server utilizzando i cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="322a0-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="322a0-127">Per informazioni sull'utilizzo dei cmdlet, vedere la documentazione di [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="322a0-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="322a0-128">Per ulteriori informazioni sul cmdlet di Import-Module, vedere [Import-Module](/previous-versions//dd347701(v=technet.10)) nella libreria Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="322a0-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="322a0-129">Per informazioni sulla riga di comando, digitare **Get-Help Import-Module**.</span><span class="sxs-lookup"><span data-stu-id="322a0-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="322a0-130">Per ulteriori informazioni sul cmdlet di Add-WindowsFeature, vedere [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) nella libreria Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="322a0-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="322a0-131">Per informazioni sulla riga di comando, digitare **Get-Help Add-WindowsFeature**.</span><span class="sxs-lookup"><span data-stu-id="322a0-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="322a0-132">**Per installare BITS Compact Server tramite Gestione pacchetti**</span><span class="sxs-lookup"><span data-stu-id="322a0-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="322a0-133">Immettere il comando seguente: **PkgMgr.exe/IU: LightweightServer**.</span><span class="sxs-lookup"><span data-stu-id="322a0-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="322a0-134">Le impostazioni vengono perse se il servizio Compact Server viene riavviato o se il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="322a0-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="322a0-135">Gestione remota BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="322a0-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="322a0-136">BITS Compact Server con gestione remota BITS consente trasferimenti di file remoti più sicuri.</span><span class="sxs-lookup"><span data-stu-id="322a0-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="322a0-137">Gestione remota BITS usa un provider Strumentazione gestione Windows (WMI) per consentire a un amministratore di sistema o a un'applicazione controller di creare in modalità remota processi di trasferimento BITS nei client e di pubblicare file per l'hosting nel server BITS Compact.</span><span class="sxs-lookup"><span data-stu-id="322a0-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="322a0-138">Il provider BITS può essere utilizzato anche per consentire a un'applicazione di utilizzare in modalità remota il client BITS insieme a BITS Compact Server per trasferire file da un computer remoto a un altro computer remoto.</span><span class="sxs-lookup"><span data-stu-id="322a0-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="322a0-139">Per ulteriori informazioni, vedere la documentazione del [provider bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="322a0-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="322a0-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="322a0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="322a0-141">Provider BITS</span><span class="sxs-lookup"><span data-stu-id="322a0-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 