---
title: Registrazione degli errori in Windows Server 2003 SP1
description: Registrazione degli errori in Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Registrazione degli errori in Windows Server 2003 con Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/14/2019
ms.locfileid: "103719339"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="a76b4-104">Registrazione degli errori in Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="a76b4-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="a76b4-105">Aggiunta di intestazioni di stile W3C</span><span class="sxs-lookup"><span data-stu-id="a76b4-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="a76b4-106">A partire da Windows Server 2003 con Service Pack 1 (SP1), il log degli errori dell'API del server HTTP include intestazioni di stile W3C che consentono di analizzare i file di log tramite parser di log standard.</span><span class="sxs-lookup"><span data-stu-id="a76b4-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="a76b4-107">Il modello riportato di seguito elenca tutti i campi che possono essere registrati nel file di log degli errori http.</span><span class="sxs-lookup"><span data-stu-id="a76b4-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="a76b4-108">Registrazione di campi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="a76b4-108">Logging Additional Fields</span></span>

<span data-ttu-id="a76b4-109">Il log degli errori HTTP è stato esteso per includere nove più campi per registrare i dati sugli errori che si verificano.</span><span class="sxs-lookup"><span data-stu-id="a76b4-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="a76b4-110">I nuovi campi di errore sono elencati di seguito:</span><span class="sxs-lookup"><span data-stu-id="a76b4-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="a76b4-111">Nome computer server \[ S-computername\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="a76b4-112">CS agente utente \[ ( \_ agente utente)\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="a76b4-113">Cookie \[ cs (cookie)\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="a76b4-114">\[CS Referrer (referrer)\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="a76b4-115">Nome host \[ cs-host\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="a76b4-116">Byte ricevuti dal server \[ sc-bytes\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="a76b4-117">Byte ricevuti ed elaborati dal server \[ CS-bytes\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="a76b4-118">Tempo impiegato per elaborare la richiesta in \[ tempo\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="a76b4-119">Queue-Name (riservato per IIS) \[ S-QueueName\]</span><span class="sxs-lookup"><span data-stu-id="a76b4-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="a76b4-120">Selezione dei file di log per l'accesso al file di log degli errori HTTP</span><span class="sxs-lookup"><span data-stu-id="a76b4-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="a76b4-121">È stata aggiunta la chiave del registro di sistema **ErrorLoggingFields** per controllare i campi registrati nel log degli errori http.</span><span class="sxs-lookup"><span data-stu-id="a76b4-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="a76b4-122">I valori del registro di sistema si trovano in una \\ chiave di parametri http disponibile in:</span><span class="sxs-lookup"><span data-stu-id="a76b4-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="a76b4-123">Il valore del registro di sistema **ErrorLoggingFields** è un valore DWORD che contiene i valori di bit per ognuno dei campi che possono essere registrati.</span><span class="sxs-lookup"><span data-stu-id="a76b4-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="a76b4-124">Per abilitare la registrazione di un campo specifico, impostare il valore di bit corrispondente su 1 e riavviare il servizio HTTP.</span><span class="sxs-lookup"><span data-stu-id="a76b4-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="a76b4-125">Per disabilitare la registrazione, impostare il valore di bit su 0.</span><span class="sxs-lookup"><span data-stu-id="a76b4-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="a76b4-126">Per configurare più campi, utilizzare un operatore OR bit per bit dei singoli valori.</span><span class="sxs-lookup"><span data-stu-id="a76b4-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="a76b4-127">Ad esempio, per attivare il cookie e i campi di registrazione del referrer, il valore deve essere 0x00020000 \| 0x00040000 = 0x00060000.</span><span class="sxs-lookup"><span data-stu-id="a76b4-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="a76b4-128">Se la chiave del registro di sistema **ErrorLoggingFields** è assente, vengono registrati i campi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a76b4-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="a76b4-129">Il valore di **ErrorLoggingFields** per la registrazione dei campi predefiniti è 0x7c884c7.</span><span class="sxs-lookup"><span data-stu-id="a76b4-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="a76b4-130">Per abilitare la registrazione per tutti i campi indicati nella tabella seguente, impostare il valore su 0x7dff4e7.</span><span class="sxs-lookup"><span data-stu-id="a76b4-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="a76b4-131">I campi di registrazione degli errori sono elencati nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="a76b4-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="a76b4-132">Campo log</span><span class="sxs-lookup"><span data-stu-id="a76b4-132">Log field</span></span>            | <span data-ttu-id="a76b4-133">Registrato per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="a76b4-133">Logged by default</span></span> | <span data-ttu-id="a76b4-134">Valore bit</span><span class="sxs-lookup"><span data-stu-id="a76b4-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="a76b4-135">Data</span><span class="sxs-lookup"><span data-stu-id="a76b4-135">Date</span></span>                 | <span data-ttu-id="a76b4-136">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-136">Yes</span></span>               | <span data-ttu-id="a76b4-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a76b4-137">0x00000001</span></span> |
| <span data-ttu-id="a76b4-138">Tempo</span><span class="sxs-lookup"><span data-stu-id="a76b4-138">Time</span></span>                 | <span data-ttu-id="a76b4-139">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-139">Yes</span></span>               | <span data-ttu-id="a76b4-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a76b4-140">0x00000002</span></span> |
| <span data-ttu-id="a76b4-141">Nome computer server</span><span class="sxs-lookup"><span data-stu-id="a76b4-141">Server Computer Name</span></span> | <span data-ttu-id="a76b4-142">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-142">No</span></span>                | <span data-ttu-id="a76b4-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a76b4-143">0x00000020</span></span> |
| <span data-ttu-id="a76b4-144">Indirizzo IP client</span><span class="sxs-lookup"><span data-stu-id="a76b4-144">Client IP Address</span></span>    | <span data-ttu-id="a76b4-145">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-145">Yes</span></span>               | <span data-ttu-id="a76b4-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a76b4-146">0x00000004</span></span> |
| <span data-ttu-id="a76b4-147">Porta client</span><span class="sxs-lookup"><span data-stu-id="a76b4-147">Client Port</span></span>          | <span data-ttu-id="a76b4-148">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-148">Yes</span></span>               | <span data-ttu-id="a76b4-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="a76b4-149">0x00400000</span></span> |
| <span data-ttu-id="a76b4-150">Indirizzo IP del server</span><span class="sxs-lookup"><span data-stu-id="a76b4-150">Server IP Address</span></span>    | <span data-ttu-id="a76b4-151">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-151">Yes</span></span>               | <span data-ttu-id="a76b4-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="a76b4-152">0x00000040</span></span> |
| <span data-ttu-id="a76b4-153">Porta server</span><span class="sxs-lookup"><span data-stu-id="a76b4-153">Server Port</span></span>          | <span data-ttu-id="a76b4-154">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-154">Yes</span></span>               | <span data-ttu-id="a76b4-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="a76b4-155">0x00008000</span></span> |
| <span data-ttu-id="a76b4-156">Versione protocollo</span><span class="sxs-lookup"><span data-stu-id="a76b4-156">Protocol Version</span></span>     | <span data-ttu-id="a76b4-157">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-157">Yes</span></span>               | <span data-ttu-id="a76b4-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="a76b4-158">0x00080000</span></span> |
| <span data-ttu-id="a76b4-159">Metodo</span><span class="sxs-lookup"><span data-stu-id="a76b4-159">Method</span></span>               | <span data-ttu-id="a76b4-160">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-160">Yes</span></span>               | <span data-ttu-id="a76b4-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a76b4-161">0x00000080</span></span> |
| <span data-ttu-id="a76b4-162">URI</span><span class="sxs-lookup"><span data-stu-id="a76b4-162">URI</span></span>                  | <span data-ttu-id="a76b4-163">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-163">Yes</span></span>               | <span data-ttu-id="a76b4-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="a76b4-164">0x00800000</span></span> |
| <span data-ttu-id="a76b4-165">Agente utente</span><span class="sxs-lookup"><span data-stu-id="a76b4-165">User Agent</span></span>           | <span data-ttu-id="a76b4-166">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-166">No</span></span>                | <span data-ttu-id="a76b4-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="a76b4-167">0x00010000</span></span> |
| <span data-ttu-id="a76b4-168">Cookie</span><span class="sxs-lookup"><span data-stu-id="a76b4-168">Cookie</span></span>               | <span data-ttu-id="a76b4-169">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-169">No</span></span>                | <span data-ttu-id="a76b4-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="a76b4-170">0x00020000</span></span> |
| <span data-ttu-id="a76b4-171">Referrer</span><span class="sxs-lookup"><span data-stu-id="a76b4-171">referrer</span></span>             | <span data-ttu-id="a76b4-172">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-172">No</span></span>                | <span data-ttu-id="a76b4-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="a76b4-173">0x00040000</span></span> |
| <span data-ttu-id="a76b4-174">Host</span><span class="sxs-lookup"><span data-stu-id="a76b4-174">Host</span></span>                 | <span data-ttu-id="a76b4-175">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-175">No</span></span>                | <span data-ttu-id="a76b4-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="a76b4-176">0x00100000</span></span> |
| <span data-ttu-id="a76b4-177">Stato protocollo</span><span class="sxs-lookup"><span data-stu-id="a76b4-177">Protocol Status</span></span>      | <span data-ttu-id="a76b4-178">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-178">Yes</span></span>               | <span data-ttu-id="a76b4-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="a76b4-179">0x00000400</span></span> |
| <span data-ttu-id="a76b4-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="a76b4-180">SC-Bytes</span></span>             | <span data-ttu-id="a76b4-181">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-181">No</span></span>                | <span data-ttu-id="a76b4-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="a76b4-182">0x00001000</span></span> |
| <span data-ttu-id="a76b4-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="a76b4-183">CS-Bytes</span></span>             | <span data-ttu-id="a76b4-184">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-184">No</span></span>                | <span data-ttu-id="a76b4-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="a76b4-185">0x00002000</span></span> |
| <span data-ttu-id="a76b4-186">Tempo impiegato</span><span class="sxs-lookup"><span data-stu-id="a76b4-186">Time Taken</span></span>           | <span data-ttu-id="a76b4-187">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-187">No</span></span>                | <span data-ttu-id="a76b4-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="a76b4-188">0x00004000</span></span> |
| <span data-ttu-id="a76b4-189">SiteId</span><span class="sxs-lookup"><span data-stu-id="a76b4-189">SiteId</span></span>               | <span data-ttu-id="a76b4-190">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-190">Yes</span></span>               | <span data-ttu-id="a76b4-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="a76b4-191">0x01000000</span></span> |
| <span data-ttu-id="a76b4-192">Frase motivo</span><span class="sxs-lookup"><span data-stu-id="a76b4-192">Reason Phrase</span></span>        | <span data-ttu-id="a76b4-193">Sì</span><span class="sxs-lookup"><span data-stu-id="a76b4-193">Yes</span></span>               | <span data-ttu-id="a76b4-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="a76b4-194">0x02000000</span></span> |
| <span data-ttu-id="a76b4-195">Nome coda</span><span class="sxs-lookup"><span data-stu-id="a76b4-195">Queue Name</span></span>           | <span data-ttu-id="a76b4-196">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-196">No</span></span>                | <span data-ttu-id="a76b4-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="a76b4-197">0x04000000</span></span> |
| <span data-ttu-id="a76b4-198">ID flusso</span><span class="sxs-lookup"><span data-stu-id="a76b4-198">Stream Id</span></span>            | <span data-ttu-id="a76b4-199">No</span><span class="sxs-lookup"><span data-stu-id="a76b4-199">No</span></span>                | <span data-ttu-id="a76b4-200">0x????????</span><span class="sxs-lookup"><span data-stu-id="a76b4-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="a76b4-201">Rollover di data e ora</span><span class="sxs-lookup"><span data-stu-id="a76b4-201">Time and Date Rollover</span></span>

<span data-ttu-id="a76b4-202">Per impostazione predefinita, viene creato un nuovo file di log degli errori HTTP (denominato rollover dei file) quando il file di log corrente raggiunge una dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="a76b4-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="a76b4-203">A partire da Windows Server 2003 con SP1, è possibile creare nuovi file di log degli errori in base alla data e all'ora.</span><span class="sxs-lookup"><span data-stu-id="a76b4-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="a76b4-204">Il rollover di data e ora è controllato da due nuovi valori del registro di sistema: **ErrorLoggingRolloverType** e **ErrorLoggingLocaltimeRollover**.</span><span class="sxs-lookup"><span data-stu-id="a76b4-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="a76b4-205">Per abilitare il rollover di data e ora, questi valori del registro di sistema devono essere aggiunti al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a76b4-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="a76b4-206">Il servizio HTTP deve essere riavviato quando queste chiavi vengono aggiunte al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a76b4-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="a76b4-207">Le chiavi del registro di sistema per il rollover dei file di log vengono create nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="a76b4-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="a76b4-208">La chiave del registro di sistema **ErrorLoggingRolloverType** indica il tipo di rollover desiderato e per impostazione predefinita è impostato sul rollover basato sulle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a76b4-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="a76b4-209">Il rollover può anche essere impostato in modo da essere eseguito su base giornaliera, settimanale, mensile o oraria.</span><span class="sxs-lookup"><span data-stu-id="a76b4-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="a76b4-210">Quando il rollover dei file è basato sul tempo, un valore **ErrorLoggingLocaltimeRollover** pari a 0 indica che il tempo di rollover è espresso in GMT e il valore 1 indica che il tempo di rollover è espresso nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="a76b4-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="a76b4-211">La chiave **ErrorLoggingRolloverType** può assumere un valore compreso tra 0 e 4, come elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a76b4-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="a76b4-212">Valore tipo di rollover</span><span class="sxs-lookup"><span data-stu-id="a76b4-212">Rollover type value</span></span> | <span data-ttu-id="a76b4-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a76b4-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76b4-214">0</span><span class="sxs-lookup"><span data-stu-id="a76b4-214">0</span></span>                   | <span data-ttu-id="a76b4-215">Rollover basato sulle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a76b4-215">Size based rollover.</span></span> <span data-ttu-id="a76b4-216">Viene eseguito il rollover dei file di log quando il file raggiunge le dimensioni definite nella chiave del registro di sistema **ErrorLogFileTruncateSize** .</span><span class="sxs-lookup"><span data-stu-id="a76b4-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="a76b4-217">1</span><span class="sxs-lookup"><span data-stu-id="a76b4-217">1</span></span>                   | <span data-ttu-id="a76b4-218">Il rollover dei file di log viene eseguito ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="a76b4-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="a76b4-219">2</span><span class="sxs-lookup"><span data-stu-id="a76b4-219">2</span></span>                   | <span data-ttu-id="a76b4-220">Il rollover dei file di log viene eseguito settimanalmente.</span><span class="sxs-lookup"><span data-stu-id="a76b4-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="a76b4-221">3</span><span class="sxs-lookup"><span data-stu-id="a76b4-221">3</span></span>                   | <span data-ttu-id="a76b4-222">Il rollover dei file di log viene eseguito mensilmente.</span><span class="sxs-lookup"><span data-stu-id="a76b4-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="a76b4-223">4</span><span class="sxs-lookup"><span data-stu-id="a76b4-223">4</span></span>                   | <span data-ttu-id="a76b4-224">Il rollover dei file di log viene eseguito ogni ora.</span><span class="sxs-lookup"><span data-stu-id="a76b4-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="a76b4-225">Le convenzioni di denominazione per i file in cui sono archiviati i log degli errori sono diverse per le dimensioni, la data e il rollover basato sull'ora.</span><span class="sxs-lookup"><span data-stu-id="a76b4-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="a76b4-226">Nella tabella seguente sono elencate le convenzioni di denominazione per i file di log http.</span><span class="sxs-lookup"><span data-stu-id="a76b4-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="a76b4-227">Tipo Tollover</span><span class="sxs-lookup"><span data-stu-id="a76b4-227">Tollover type</span></span> | <span data-ttu-id="a76b4-228">Nome file di log</span><span class="sxs-lookup"><span data-stu-id="a76b4-228">Log file name</span></span>  | <span data-ttu-id="a76b4-229">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a76b4-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76b4-230">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a76b4-230">Size</span></span>          | <span data-ttu-id="a76b4-231">HTTPERRn. LOG</span><span class="sxs-lookup"><span data-stu-id="a76b4-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="a76b4-232">Il file di log viene riciclato quando raggiunge una dimensione specifica.</span><span class="sxs-lookup"><span data-stu-id="a76b4-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="a76b4-233">n è il numero di file e viene incrementato quando viene eseguito il rollover del file di log.</span><span class="sxs-lookup"><span data-stu-id="a76b4-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="a76b4-234">Ogni giorno</span><span class="sxs-lookup"><span data-stu-id="a76b4-234">Daily</span></span>         | <span data-ttu-id="a76b4-235">htYYMMDD. log</span><span class="sxs-lookup"><span data-stu-id="a76b4-235">htYYMMDD.log</span></span>   | <span data-ttu-id="a76b4-236">Il file di log viene riciclato quotidianamente.</span><span class="sxs-lookup"><span data-stu-id="a76b4-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="a76b4-237">Settimanale</span><span class="sxs-lookup"><span data-stu-id="a76b4-237">Weekly</span></span>        | <span data-ttu-id="a76b4-238">htYYMMww. log</span><span class="sxs-lookup"><span data-stu-id="a76b4-238">htYYMMww.log</span></span>   | <span data-ttu-id="a76b4-239">Il file di log viene riciclato settimanalmente, dove WW è la settimana del mese.</span><span class="sxs-lookup"><span data-stu-id="a76b4-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="a76b4-240">Ogni mese</span><span class="sxs-lookup"><span data-stu-id="a76b4-240">Monthly</span></span>       | <span data-ttu-id="a76b4-241">htYYMM. log</span><span class="sxs-lookup"><span data-stu-id="a76b4-241">htYYMM.log</span></span>     | <span data-ttu-id="a76b4-242">Il file di log viene riciclato ogni mese.</span><span class="sxs-lookup"><span data-stu-id="a76b4-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="a76b4-243">Ogni ora</span><span class="sxs-lookup"><span data-stu-id="a76b4-243">Hourly</span></span>        | <span data-ttu-id="a76b4-244">htYYMMDDhh. log</span><span class="sxs-lookup"><span data-stu-id="a76b4-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="a76b4-245">Il file di log viene riciclato ogni ora, dove HH è l'ora del giorno espressa in notazione di 0-24 ore.</span><span class="sxs-lookup"><span data-stu-id="a76b4-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




