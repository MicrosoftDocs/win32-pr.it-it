---
description: Se il client e l'host non possono scambiare metadati, è possibile sostituire un host e un client generici per l'host e il client personalizzati, in modo da consentire la risoluzione del problema.
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: Uso di un host e di un client generici per lo scambio di metadati HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308832"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="5788b-103">Uso di un host e di un client generici per lo scambio di metadati HTTP</span><span class="sxs-lookup"><span data-stu-id="5788b-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="5788b-104">Se il client e l'host non possono scambiare metadati, è possibile sostituire un host e un client generici per l'host e il client personalizzati, in modo da consentire la risoluzione del problema.</span><span class="sxs-lookup"><span data-stu-id="5788b-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="5788b-105">Se l'indirizzo del dispositivo o i metadati del dispositivo non vengono visualizzati nell'output del client di debug WSD, è possibile che l'errore venga causato dagli indirizzi di trasporto o dall'ambiente di rete specificati.</span><span class="sxs-lookup"><span data-stu-id="5788b-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="5788b-106">Per ulteriori informazioni sull'host e sul client generico, vedere [strumenti di debug](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5788b-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="5788b-107">Se è stato verificato che un host e un client generici possono completare sia WS-Discovery che lo scambio di metadati HTTP, questa procedura di diagnostica può essere ignorata e la risoluzione dei problemi può proseguire seguendo le procedure descritte in [uso della registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="5788b-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="5788b-108">Se l'host o il client è un'applicazione in esecuzione in un computer, l'host o il client generico deve essere eseguito nello stesso contesto di sicurezza dell'host o del client effettivo.</span><span class="sxs-lookup"><span data-stu-id="5788b-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="5788b-109">Se, ad esempio, l'host o il client effettivo viene eseguito come amministratore, l'host o il client generico deve essere eseguito come amministratore.</span><span class="sxs-lookup"><span data-stu-id="5788b-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="5788b-110">Inoltre, se l'host o il client è un dispositivo autonomo, deve essere completamente sostituito da un PC che esegue un host o un client generico in un contesto di sicurezza che garantisce un accesso illimitato alla rete (ad esempio, in esecuzione come amministratore).</span><span class="sxs-lookup"><span data-stu-id="5788b-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="5788b-111">**Per utilizzare un host e un client generici per risolvere i problemi relativi allo scambio di metadati HTTP**</span><span class="sxs-lookup"><span data-stu-id="5788b-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="5788b-112">Aprire una finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="5788b-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="5788b-113">Eseguire il comando seguente: **WSDDebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="5788b-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="5788b-114">Potrebbe essere visualizzata una finestra di dialogo **avviso di sicurezza di Windows** .</span><span class="sxs-lookup"><span data-stu-id="5788b-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="5788b-115">In tal caso, fare clic su **Sblocca** per consentire l'esecuzione dell'host di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="5788b-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="5788b-116">Questo comando genera un output simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="5788b-116">This command generates output similar to the following.</span></span> <span data-ttu-id="5788b-117">Prendere nota dell'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5788b-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="5788b-118">Eseguire il comando seguente: **WSDDebug \_client.exe/Mode Metadata/Hello off/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="5788b-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="5788b-119">Sostituire *<id>* con l'ID dispositivo identificato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="5788b-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="5788b-120">Potrebbe essere visualizzata una finestra di dialogo **avviso di sicurezza di Windows** .</span><span class="sxs-lookup"><span data-stu-id="5788b-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="5788b-121">In tal caso, fare clic su **Sblocca** per consentire l'esecuzione del client di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="5788b-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="5788b-122">Il client di debug WSD genera un output simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="5788b-122">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="5788b-123">Il client di debug WSD può generare molti output in una rete con molti dispositivi DPWS.</span><span class="sxs-lookup"><span data-stu-id="5788b-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="5788b-124">L'output può essere reindirizzato a un file per semplificare l'analisi.</span><span class="sxs-lookup"><span data-stu-id="5788b-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="5788b-125">Digitare **log Tee** *<filename>* al prompt del client di debug WSD per reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="5788b-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="5788b-126">È possibile arrestare il reindirizzamento dell'output digitando **log Tee stop** al prompt del client di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="5788b-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="5788b-127">Prendere nota dell'indirizzo EPR (endpoint Reference).</span><span class="sxs-lookup"><span data-stu-id="5788b-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="5788b-128">Questo indirizzo EPR deve corrispondere all'ID dispositivo identificato nel passaggio 2 precedente.</span><span class="sxs-lookup"><span data-stu-id="5788b-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="5788b-129">Verificare inoltre che il client di debug WSD abbia stampato completamente i metadati per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5788b-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="5788b-130">I metadati del dispositivo iniziano con `Metadata for host` e terminano con `End of metadata` .</span><span class="sxs-lookup"><span data-stu-id="5788b-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="5788b-131">Se l'ID dispositivo e i metadati del dispositivo vengono visualizzati correttamente nell'output del client di debug WSD, è probabile che l'errore dell'applicazione non sia correlato agli indirizzi di trasporto, al sistema operativo o all'ambiente di rete specificati.</span><span class="sxs-lookup"><span data-stu-id="5788b-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="5788b-132">Sostituire l'host e il client generici con l'host e il client personalizzati e continuare la risoluzione dei problemi seguendo le procedure descritte in [uso della registrazione WinHTTP per verificare il traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="5788b-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="5788b-133">Se l'indirizzo del dispositivo e i metadati del dispositivo non vengono visualizzati nell'output del client di debug WSD, l'errore può avere una o più delle cause seguenti:</span><span class="sxs-lookup"><span data-stu-id="5788b-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="5788b-134">L'indirizzo di trasporto annunciato dall'host non è corretto o non è valido.</span><span class="sxs-lookup"><span data-stu-id="5788b-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="5788b-135">Il client di debug WSD tenta di ottenere i metadati del dispositivo dall'URL fornito nell'elemento **XAddrs** di un messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="5788b-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="5788b-136">L'URL utilizzato per lo scambio di metadati viene visualizzato nell'output del client di debug WSD, preceduto dalla frase `Using xAddr` .</span><span class="sxs-lookup"><span data-stu-id="5788b-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="5788b-137">Nell'esempio seguente vengono illustrati i XAddrs utilizzati per lo scambio di metadati nell'output del client di debug WSD precedente.</span><span class="sxs-lookup"><span data-stu-id="5788b-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="5788b-138">Se il XAddrs fornito non è conforme alle [regole di convalida XAddr](xaddr-validation-rules.md), il client di debug WSD non è in grado di ottenere i metadati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5788b-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="5788b-139">L'applicazione viene eseguita nel contesto di sicurezza errato.</span><span class="sxs-lookup"><span data-stu-id="5788b-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="5788b-140">Verificare che l'applicazione utilizzi le credenziali corrette e che il client e l'host dispongano delle autorizzazioni sufficienti per accedere alla rete.</span><span class="sxs-lookup"><span data-stu-id="5788b-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="5788b-141">La configurazione del firewall non è corretta.</span><span class="sxs-lookup"><span data-stu-id="5788b-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="5788b-142">Seguire le istruzioni riportate in [ispezione delle impostazioni di adapter e firewall](inspecting-adapter-and-firewall-settings.md) per verificare che le impostazioni Windows Firewall siano corrette e che non siano presenti altre regole che eliminano i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5788b-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="5788b-143">Il client e l'host possono anche essere copiati in un computer "incontaminato" (uno con un'installazione predefinita del sistema operativo che non è mai stato aggiunto a un dominio) per tentare di riprodurre l'errore.</span><span class="sxs-lookup"><span data-stu-id="5788b-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="5788b-144">Un criterio IPSec blocca l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5788b-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="5788b-145">Copiare il client e l'host su un computer che non è soggetto ai criteri IPSec e provare a riprodurre l'errore.</span><span class="sxs-lookup"><span data-stu-id="5788b-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5788b-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5788b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5788b-147">Procedure di diagnostica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="5788b-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="5788b-148">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="5788b-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



