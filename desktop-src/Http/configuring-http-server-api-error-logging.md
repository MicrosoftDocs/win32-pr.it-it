---
title: Configurazione della registrazione degli errori dell'API del server HTTP
description: La registrazione degli errori dell'API del server HTTP è controllata da tre valori del registro di sistema in una \\ chiave di parametri http.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API server HTTP, configurazione dei log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395931"
---
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="a5886-104">Configurazione della registrazione degli errori dell'API del server HTTP</span><span class="sxs-lookup"><span data-stu-id="a5886-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="a5886-105">La registrazione degli errori dell'API del server http è controllata da tre valori del registro di sistema in una chiave di \\ **parametri** http disponibile in:</span><span class="sxs-lookup"><span data-stu-id="a5886-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="a5886-106">Il percorso e il formato dei valori di configurazione possono cambiare nelle versioni future del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="a5886-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="a5886-107">Un utente deve disporre dei privilegi di amministratore/sistema locale per modificare i valori del registro di sistema e visualizzare o modificare i file di log e la cartella che li contiene.</span><span class="sxs-lookup"><span data-stu-id="a5886-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="a5886-108">Le informazioni di configurazione nei valori del registro di sistema vengono lette all'avvio del driver dell'API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="a5886-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="a5886-109">Di conseguenza, se le impostazioni vengono modificate, il driver deve essere arrestato e riavviato per leggere i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="a5886-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="a5886-110">Questa operazione può essere eseguita usando i comandi seguenti della console:</span><span class="sxs-lookup"><span data-stu-id="a5886-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="a5886-111">**NET stop http**</span><span class="sxs-lookup"><span data-stu-id="a5886-111">**net stop http**</span></span>

<span data-ttu-id="a5886-112">**NET start http**</span><span class="sxs-lookup"><span data-stu-id="a5886-112">**net start http**</span></span>

<span data-ttu-id="a5886-113">I file di log vengono denominati usando la convenzione seguente:</span><span class="sxs-lookup"><span data-stu-id="a5886-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="a5886-114">**HTTPERR +** *SequenceNumber* **+. log**</span><span class="sxs-lookup"><span data-stu-id="a5886-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="a5886-115">Ad esempio: "httperr4. log".</span><span class="sxs-lookup"><span data-stu-id="a5886-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="a5886-116">I file di log vengono ciclati quando raggiungono la dimensione massima specificata dal valore del registro di sistema **ErrorLogFileTruncateSize** e il valore non può essere minore di un megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="a5886-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="a5886-117">Se la configurazione della registrazione degli errori non è valida o si verifica un qualsiasi tipo di errore durante la scrittura nei file di log, l'API del server HTTP usa la registrazione degli eventi per notificare agli amministratori che la registrazione degli errori non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="a5886-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="a5886-118">Nella tabella seguente sono descritti i valori di configurazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a5886-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a5886-119">Valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a5886-119">Registry Value</span></span></th>
<th><span data-ttu-id="a5886-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5886-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5886-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span><span class="sxs-lookup"><span data-stu-id="a5886-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="a5886-122"><strong>Valore DWORD</strong> che può essere impostato su <strong>true</strong> per abilitare la registrazione degli errori oppure <strong>false</strong> per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="a5886-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="a5886-123">Il valore predefinito è <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5886-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5886-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span><span class="sxs-lookup"><span data-stu-id="a5886-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="a5886-125"><strong>Valore DWORD</strong> che specifica la dimensione massima in byte del file di log degli errori.</span><span class="sxs-lookup"><span data-stu-id="a5886-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="a5886-126">Il valore predefinito è 1 MB (0x100000).</span><span class="sxs-lookup"><span data-stu-id="a5886-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a5886-127">Il valore specificato non può essere minore del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a5886-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5886-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span><span class="sxs-lookup"><span data-stu-id="a5886-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="a5886-129"><strong>Stringa</strong> che specifica la cartella in cui l'API del server http inserisce i file di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a5886-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="a5886-130">L'API server HTTP crea una sottocartella denominata &quot; HTTPERR nella &quot; cartella specificata in cui vengono inseriti i file di log.</span><span class="sxs-lookup"><span data-stu-id="a5886-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="a5886-131">Questa sottocartella e i file di log ricevono le stesse impostazioni di autorizzazione, il che significa che gli account amministratore e di sistema locale hanno accesso completo, mentre altri utenti non hanno accesso.</span><span class="sxs-lookup"><span data-stu-id="a5886-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="a5886-132">Se una cartella non è specificata nel registro di sistema, la cartella predefinita è la seguente:</span><span class="sxs-lookup"><span data-stu-id="a5886-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="a5886-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="a5886-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a5886-134">Il valore della stringa ErrorLoggingDir deve essere un percorso completo, ma può contenere &quot; % systemroot% &quot; .</span><span class="sxs-lookup"><span data-stu-id="a5886-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





