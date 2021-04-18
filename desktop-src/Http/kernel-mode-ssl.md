---
title: SSL in modalità kernel
description: SSL in modalità kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL in modalità kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298821"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="b6306-104">SSL in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="b6306-104">Kernel Mode SSL</span></span>

<span data-ttu-id="b6306-105">La modalità kernel SSL è stata introdotta in Windows Server 2003 con Service Pack 1 (SP1) con supporto limitato.</span><span class="sxs-lookup"><span data-stu-id="b6306-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="b6306-106">Per i computer in cui è in esecuzione Windows Server 2003 con SP1, è necessario impostare una chiave del registro di sistema per abilitare il kernel SSL.</span><span class="sxs-lookup"><span data-stu-id="b6306-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="b6306-107">Per i computer che eseguono Windows Server 2008 e Windows Vista, è disponibile il supporto completo della modalità kernel per SSL.</span><span class="sxs-lookup"><span data-stu-id="b6306-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="b6306-108">Nelle sezioni seguenti viene descritto il supporto SSL in modalità kernel:</span><span class="sxs-lookup"><span data-stu-id="b6306-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="b6306-109">Modalità kernel SSL in Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="b6306-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="b6306-110">SSL in modalità kernel in Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6306-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="b6306-111">Modalità kernel SSL in Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="b6306-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="b6306-112">In Windows Server 2003 con SP1, l'API server HTTP fornisce la possibilità di eseguire la protezione SSL in modalità kernel (l'impostazione predefinita è SSL in modalità utente).</span><span class="sxs-lookup"><span data-stu-id="b6306-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="b6306-113">La funzionalità modalità kernel migliora le prestazioni SSL spostando le operazioni di crittografia e decrittografia nel kernel, riducendo così il numero di transizioni tra la modalità kernel e la modalità utente.</span><span class="sxs-lookup"><span data-stu-id="b6306-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="b6306-114">Le funzionalità seguenti non sono supportate quando SSL viene eseguito in modalità kernel:</span><span class="sxs-lookup"><span data-stu-id="b6306-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="b6306-115">Certificati client</span><span class="sxs-lookup"><span data-stu-id="b6306-115">Client certificates</span></span>
-   <span data-ttu-id="b6306-116">Crittografie RC2</span><span class="sxs-lookup"><span data-stu-id="b6306-116">RC2 ciphers</span></span>
-   <span data-ttu-id="b6306-117">Protocollo PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="b6306-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="b6306-118">Le modifiche alla configurazione del certificato server richiedono il riavvio del servizio HTTP</span><span class="sxs-lookup"><span data-stu-id="b6306-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="b6306-119">Supporto per la crittografia e l'offload bulk</span><span class="sxs-lookup"><span data-stu-id="b6306-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="b6306-120">Configurazione di SSL in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="b6306-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="b6306-121">Il protocollo SSL in modalità kernel è controllato dal valore del registro di sistema **EnableKernelSSL** e viene abilitato impostando il valore su 1.</span><span class="sxs-lookup"><span data-stu-id="b6306-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="b6306-122">L'abilitazione di SSL in modalità kernel Disabilita SSL in modalità utente e richiede il riavvio del servizio HTTP per renderlo effettivo.</span><span class="sxs-lookup"><span data-stu-id="b6306-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="b6306-123">La chiave del registro di sistema **EnableKernelSSL** si trova in:</span><span class="sxs-lookup"><span data-stu-id="b6306-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="b6306-124">**HKEY \_ \_** \\  \\  \\  \\  \\ **Parametri** http dei servizi \\  CurrentControlSet del sistema del computer locale EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="b6306-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="b6306-125">SSL in modalità kernel in Windows Server 2008 e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6306-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="b6306-126">Per i computer che eseguono Windows Server 2008 e Windows Vista, l'API server HTTP offre funzionalità SSL avanzate.</span><span class="sxs-lookup"><span data-stu-id="b6306-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="b6306-127">Sono supportate le seguenti nuove funzionalità:</span><span class="sxs-lookup"><span data-stu-id="b6306-127">The following new features are supported:</span></span>

-   <span data-ttu-id="b6306-128">Supporto completo del certificato client in modalità kernel SSL</span><span class="sxs-lookup"><span data-stu-id="b6306-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="b6306-129">SSL in modalità kernel per tutte le transazioni SSL HTTP</span><span class="sxs-lookup"><span data-stu-id="b6306-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="b6306-130">Supporto per la crittografia e l'offload bulk</span><span class="sxs-lookup"><span data-stu-id="b6306-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="b6306-131">Protocollo PCT 1,0</span><span class="sxs-lookup"><span data-stu-id="b6306-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="b6306-132">Crittografie RC2</span><span class="sxs-lookup"><span data-stu-id="b6306-132">RC2 ciphers</span></span>
-   <span data-ttu-id="b6306-133">Miglioramento delle prestazioni in modalità utente SSL</span><span class="sxs-lookup"><span data-stu-id="b6306-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="b6306-134">Configurazione</span><span class="sxs-lookup"><span data-stu-id="b6306-134">Configuration</span></span>

<span data-ttu-id="b6306-135">La modalità kernel SSL può essere configurata tramite due valori del registro di sistema nella chiave Parameters HTTP disponibile in:</span><span class="sxs-lookup"><span data-stu-id="b6306-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="b6306-136">Un utente deve disporre dei privilegi di amministratore/sistema locale per modificare i valori del registro di sistema e visualizzare o modificare i file di log e la cartella che li contiene.</span><span class="sxs-lookup"><span data-stu-id="b6306-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="b6306-137">Le informazioni di configurazione nei valori del registro di sistema vengono lette all'avvio del driver dell'API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="b6306-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="b6306-138">Di conseguenza, se le impostazioni vengono modificate, il driver deve essere arrestato e riavviato per leggere i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="b6306-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="b6306-139">Questa operazione può essere eseguita usando i comandi seguenti della console:</span><span class="sxs-lookup"><span data-stu-id="b6306-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="b6306-140">**NET stop http**</span><span class="sxs-lookup"><span data-stu-id="b6306-140">**net stop http**</span></span>

<span data-ttu-id="b6306-141">**NET start http**</span><span class="sxs-lookup"><span data-stu-id="b6306-141">**net start http**</span></span>

<span data-ttu-id="b6306-142">Nella tabella seguente sono elencati i valori di configurazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b6306-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6306-143">Valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b6306-143">Registry Value</span></span></th>
<th><span data-ttu-id="b6306-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6306-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6306-145">EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="b6306-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="b6306-146"><strong>Windows Server 2008 e Windows Vista:</strong> Questo valore del registro di sistema è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b6306-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6306-147">EnableSslCloseNotify</span><span class="sxs-lookup"><span data-stu-id="b6306-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="b6306-148">Valore <strong>DWORD</strong> impostato su <strong>true</strong> per abilitare la notifica di chiusura o <strong>false</strong> per disabilitare il requisito di chiusura della notifica.</span><span class="sxs-lookup"><span data-stu-id="b6306-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="b6306-149">Close-Notify è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b6306-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="b6306-150">Quando Close-Notify è abilitato, è necessario che l'applicazione client invii un messaggio di notifica di chiusura prima di chiudere le connessioni TCP.</span><span class="sxs-lookup"><span data-stu-id="b6306-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="b6306-151">L'API server HTTP invia anche una notifica di chiusura prima di chiudere la connessione.</span><span class="sxs-lookup"><span data-stu-id="b6306-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="b6306-152">Quando Close-Notify è abilitato e il client invia un messaggio di notifica di chiusura, l'API server HTTP riutilizzerà la sessione SSL nelle future connessioni al client.</span><span class="sxs-lookup"><span data-stu-id="b6306-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="b6306-153">Se il client non invia una notifica di chiusura, l'API del server HTTP non riutilizzerà la stessa sessione SSL per le connessioni future.</span><span class="sxs-lookup"><span data-stu-id="b6306-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="b6306-154">Pertanto, un handshake SSL completo viene attivato sulla nuova connessione, riducendo così le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b6306-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b6306-155">L'abilitazione di Close-Notify contribuisce a ridurre gli attacchi di troncamento contro le richieste e le risposte HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b6306-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="b6306-156">Quando Close-Notify è disabilitato, l'API server HTTP riutilizza la sessione SSL per le connessioni future.</span><span class="sxs-lookup"><span data-stu-id="b6306-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6306-157">DisableSslCertChainCacheOnlyUrlRetrieval</span><span class="sxs-lookup"><span data-stu-id="b6306-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="b6306-158">Valore <strong>DWORD</strong> impostato su <strong>true</strong> per consentire all'API del server http di recuperare i certificati intermedi da Internet o dall'archivio locale oppure <strong>false</strong> per recuperare i certificati intermedi solo dall'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="b6306-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="b6306-159">Il valore predefinito del registro di sistema è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6306-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="b6306-160">Per impostazione predefinita, l'API server HTTP compila una catena di certificati client recuperando i certificati intermedi dall'archivio Autorità di certificazione intermedio nell'account del computer locale.</span><span class="sxs-lookup"><span data-stu-id="b6306-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="b6306-161">L'impostazione di questo valore su <strong>true</strong> consente all'API del server http di recuperare i certificati intermedi non solo dall'archivio locale, ma anche dall'autorità di certificazione intermedia su Internet.</span><span class="sxs-lookup"><span data-stu-id="b6306-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





