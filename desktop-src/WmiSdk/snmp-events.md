---
description: Il provider SNMP supporta la scrittura nei file di log e nel debugger.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309881"
---
# <a name="snmp-events"></a><span data-ttu-id="26214-103">Eventi SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-103">SNMP Events</span></span>

<span data-ttu-id="26214-104">Il provider SNMP supporta la scrittura nei file di log e nel debugger.</span><span class="sxs-lookup"><span data-stu-id="26214-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="26214-105">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="26214-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="26214-106">Un numero di chiavi e valori del registro di sistema definisce il livello e il tipo di registrazione attualmente in corso di generazione:</span><span class="sxs-lookup"><span data-stu-id="26214-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="26214-107">Debug</span><span class="sxs-lookup"><span data-stu-id="26214-107">Debugging</span></span>

    <span data-ttu-id="26214-108">La chiave del registro di sistema **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Registration** contiene il valore di registrazione che indica se è possibile scrivere le informazioni nel debugger.</span><span class="sxs-lookup"><span data-stu-id="26214-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="26214-109">Il valore di registrazione è impostato su 0 per disabilitare l'output del debug o 1 per abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="26214-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="26214-110">La registrazione è un \_ valore reg DWORD.</span><span class="sxs-lookup"><span data-stu-id="26214-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="26214-111">Registrazione</span><span class="sxs-lookup"><span data-stu-id="26214-111">Logging</span></span>

    <span data-ttu-id="26214-112">La chiave del registro di sistema **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Logging \\ WBEMSNMP** include tutte le informazioni di registrazione specifiche per il provider SNMP.</span><span class="sxs-lookup"><span data-stu-id="26214-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="26214-113">Nella tabella seguente sono elencati i valori associati a questa chiave.</span><span class="sxs-lookup"><span data-stu-id="26214-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26214-114">Valore</span><span class="sxs-lookup"><span data-stu-id="26214-114">Value</span></span></th>
<th><span data-ttu-id="26214-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26214-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26214-116">Type</span><span class="sxs-lookup"><span data-stu-id="26214-116">Type</span></span></td>
<td><span data-ttu-id="26214-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="26214-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="26214-118">Accetta uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="26214-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="26214-119">&quot;File &quot; = (impostazione predefinita) Invia l'output di debug a un file.</span><span class="sxs-lookup"><span data-stu-id="26214-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="26214-120">&quot;Debugger &quot; = Invia l'output di debug al debugger.</span><span class="sxs-lookup"><span data-stu-id="26214-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26214-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="26214-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="26214-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="26214-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="26214-123">Accetta valori integer compresi tra 1024 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="26214-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="26214-124">Il valore corrisponde alla dimensione massima consentita, in byte, per il file di log.</span><span class="sxs-lookup"><span data-stu-id="26214-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="26214-125">Se è minore di 1024, il meccanismo di registrazione utilizza un valore pari a 1024.</span><span class="sxs-lookup"><span data-stu-id="26214-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="26214-126">Per questo valore è consigliata una dimensione minima di 8 KB.</span><span class="sxs-lookup"><span data-stu-id="26214-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="26214-127">Quando il file raggiunge le dimensioni specificate da MaxFileSize, il nome del file viene anteposto a un carattere ' ~' e viene creato un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="26214-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="26214-128">Pertanto, lo spazio massimo su disco necessario per la registrazione è due volte questo valore.</span><span class="sxs-lookup"><span data-stu-id="26214-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26214-129">File</span><span class="sxs-lookup"><span data-stu-id="26214-129">File</span></span></td>
<td><span data-ttu-id="26214-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="26214-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="26214-131">Definisce il nome del file a cui viene inviato l'output di debug quando il tipo di registrazione è impostato su "file".</span><span class="sxs-lookup"><span data-stu-id="26214-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="26214-132">Il valore predefinito è " <WBEMLOGS> \wbemsnmp.log."</span><span class="sxs-lookup"><span data-stu-id="26214-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="26214-133">Se la <WBEMLOGS> Directory non può essere determinata dalla sezione del registro di sistema WMI, il valore predefinito è' c:\wbemsnmp.log '.</span><span class="sxs-lookup"><span data-stu-id="26214-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="26214-134">Se viene utilizzata una condivisione, ad esempio \\ machine\share\wbemsnmp.log o M:\wbemsnmp.log dove M: è \\ machine\share, l'account di sistema locale in cui è in esecuzione WMI deve disporre dei diritti di accesso in lettura/scrittura al \\ machine\share.</span><span class="sxs-lookup"><span data-stu-id="26214-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26214-135">Level</span><span class="sxs-lookup"><span data-stu-id="26214-135">Level</span></span></td>
<td><span data-ttu-id="26214-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="26214-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="26214-137">Accetta valori integer compresi tra 0 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="26214-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="26214-138">Il valore è una maschera logica costituita da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="26214-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="26214-139">Le seguenti maschere di bit vengono combinate per definire il tipo di output di debug generato:</span><span class="sxs-lookup"><span data-stu-id="26214-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="26214-140">0: chiamate al metodo <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di classi SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="26214-141">1: implementazione del provider di classi SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="26214-142">2: chiamate al metodo <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di istanze SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="26214-143">3: implementazione del provider di istanze SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="26214-144">4: libreria di classi SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="26214-145">5: SNMP ARCHIVIO SMIR</span><span class="sxs-lookup"><span data-stu-id="26214-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="26214-146">6: correlatore SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="26214-147">7: codice di mapping dei tipi SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="26214-148">8: codice di threading SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="26214-149">9: implementazione e interfacce del provider di eventi SNMP</span><span class="sxs-lookup"><span data-stu-id="26214-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="26214-150">Impostare level su (2 ^ 0 + 2 ^ 8 =) 257 per le operazioni che interessano le chiamate ai metodi <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del provider di classi SNMP e operazioni utilizzando il codice di threading SNMP.</span><span class="sxs-lookup"><span data-stu-id="26214-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




