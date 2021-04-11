---
description: Se il client e l'host non possono vedersi reciprocamente sulla rete, un host e un client generici possono sostituire l'host e il client personalizzati per risolvere il problema.
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: Uso di un host e un client generici per UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226472"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a><span data-ttu-id="2761e-103">Uso di un host e un client generici per UDP WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="2761e-103">Using a Generic Host and Client for UDP WS-Discovery</span></span>

<span data-ttu-id="2761e-104">Se il client e l'host non possono vedersi reciprocamente sulla rete, un host e un client generici possono sostituire l'host e il client personalizzati per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="2761e-104">If the client and host cannot see each other on the network, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="2761e-105">Se l'indirizzo del dispositivo non viene visualizzato nell'output del client di debug WSD, è probabile che l'ambiente di rete provochi l'errore.</span><span class="sxs-lookup"><span data-stu-id="2761e-105">If the device address does not appear in the WSD Debug Client output, then the network environment is probably causing the failure.</span></span> <span data-ttu-id="2761e-106">Per ulteriori informazioni sull'host e sul client generico, vedere [strumenti di debug](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2761e-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="2761e-107">Se l'host o il client è un'applicazione in esecuzione in un computer, l'host o il client generico deve essere eseguito nello stesso contesto di sicurezza dell'host o del client effettivo.</span><span class="sxs-lookup"><span data-stu-id="2761e-107">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="2761e-108">Se, ad esempio, l'host o il client effettivo viene eseguito come amministratore, l'host o il client generico deve essere eseguito come amministratore.</span><span class="sxs-lookup"><span data-stu-id="2761e-108">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="2761e-109">Inoltre, se l'host o il client è un dispositivo autonomo, deve essere completamente sostituito da un PC che esegue un host o un client generico.</span><span class="sxs-lookup"><span data-stu-id="2761e-109">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client.</span></span>

<span data-ttu-id="2761e-110">**Per utilizzare un host e un client generici per risolvere i problemi relativi a WS-Discovery UDP**</span><span class="sxs-lookup"><span data-stu-id="2761e-110">**To using a generic host and client to troubleshoot UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="2761e-111">Aprire una finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="2761e-111">Open a command prompt window.</span></span>
2.  <span data-ttu-id="2761e-112">Eseguire il comando seguente: **WSDDebug \_host.exe/Mode Metadata/Start**</span><span class="sxs-lookup"><span data-stu-id="2761e-112">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="2761e-113">Potrebbe essere visualizzata una finestra di dialogo **avviso di sicurezza di Windows** .</span><span class="sxs-lookup"><span data-stu-id="2761e-113">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="2761e-114">In tal caso, fare clic su **Sblocca** per consentire l'esecuzione dell'host di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="2761e-114">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="2761e-115">Questo comando genera un output simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="2761e-115">This command generates output similar to the following.</span></span> <span data-ttu-id="2761e-116">Prendere nota dell'ID del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2761e-116">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="2761e-117">Eseguire il comando seguente: **WSDDebug \_client.exe/Mode Metadata/Hello off/Resolve** *<id>* .</span><span class="sxs-lookup"><span data-stu-id="2761e-117">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="2761e-118">Sostituire *<id>* con l'ID dispositivo identificato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="2761e-118">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="2761e-119">Potrebbe essere visualizzata una finestra di dialogo **avviso di sicurezza di Windows** .</span><span class="sxs-lookup"><span data-stu-id="2761e-119">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="2761e-120">In tal caso, fare clic su **Sblocca** per consentire l'esecuzione del client di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="2761e-120">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="2761e-121">Il client di debug WSD genera un output simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="2761e-121">WSD Debug Client generates output similar to the following.</span></span>

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
```

<span data-ttu-id="2761e-122">Il client di debug WSD può generare molti output in una rete con molti dispositivi DPWS.</span><span class="sxs-lookup"><span data-stu-id="2761e-122">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="2761e-123">L'output può essere reindirizzato a un file per semplificare l'analisi.</span><span class="sxs-lookup"><span data-stu-id="2761e-123">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="2761e-124">Digitare **log Tee** *<filename>* al prompt del client di debug WSD per reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="2761e-124">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="2761e-125">È possibile arrestare il reindirizzamento dell'output digitando **log Tee stop** al prompt del client di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="2761e-125">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="2761e-126">Prendere nota dell'indirizzo EPR (endpoint Reference).</span><span class="sxs-lookup"><span data-stu-id="2761e-126">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="2761e-127">Questo indirizzo EPR deve corrispondere all'ID dispositivo identificato nel passaggio 2 precedente.</span><span class="sxs-lookup"><span data-stu-id="2761e-127">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="2761e-128">In tal caso, è probabile che l'errore dell'applicazione non sia correlato al sistema operativo o all'ambiente di rete.</span><span class="sxs-lookup"><span data-stu-id="2761e-128">If this is the case, then the application failure is likely not related to the operating system or the network environment.</span></span> <span data-ttu-id="2761e-129">Sostituire l'host e il client generici con l'host e il client personalizzati e continuare la risoluzione dei problemi seguendo le procedure descritte in [utilizzo del client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="2761e-129">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

<span data-ttu-id="2761e-130">Se l'ID dispositivo non corrisponde all'indirizzo EPR, l'errore dell'applicazione è probabilmente correlato al sistema operativo o all'ambiente di rete.</span><span class="sxs-lookup"><span data-stu-id="2761e-130">If the device ID does not match the EPR address, then the application failure is probably related to the operating system or the network environment.</span></span> <span data-ttu-id="2761e-131">L'errore può avere una o più delle seguenti cause:</span><span class="sxs-lookup"><span data-stu-id="2761e-131">The failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="2761e-132">L'applicazione viene eseguita nel contesto di sicurezza errato.</span><span class="sxs-lookup"><span data-stu-id="2761e-132">The application is running in the wrong security context.</span></span> <span data-ttu-id="2761e-133">Verificare che l'applicazione utilizzi le credenziali corrette e che il client e l'host dispongano delle autorizzazioni sufficienti per accedere alla rete.</span><span class="sxs-lookup"><span data-stu-id="2761e-133">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="2761e-134">La configurazione del firewall non è corretta.</span><span class="sxs-lookup"><span data-stu-id="2761e-134">The firewall configuration is wrong.</span></span> <span data-ttu-id="2761e-135">Seguire le istruzioni riportate in [ispezione delle impostazioni di adapter e firewall](inspecting-adapter-and-firewall-settings.md) per verificare che le impostazioni Windows Firewall siano corrette e che non siano presenti altre regole che eliminano i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2761e-135">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="2761e-136">Il client e l'host possono anche essere copiati in un computer "incontaminato" (uno con un'installazione predefinita del sistema operativo che non è mai stato aggiunto a un dominio) per tentare di riprodurre l'errore.</span><span class="sxs-lookup"><span data-stu-id="2761e-136">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="2761e-137">Un criterio IPSec blocca l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2761e-137">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="2761e-138">Copiare il client e l'host su un computer non soggetto ai criteri IPSec e provare a riprodurre l'errore.</span><span class="sxs-lookup"><span data-stu-id="2761e-138">Copy the client and host onto a machine not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2761e-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2761e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2761e-140">Procedure di diagnostica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="2761e-140">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="2761e-141">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="2761e-141">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



