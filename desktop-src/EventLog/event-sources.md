---
description: Ogni log della chiave EventLog contiene sottochiavi denominate origini eventi. L'origine evento è il nome del software che registra l'evento.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Origini eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310816"
---
# <a name="event-sources"></a><span data-ttu-id="bdeda-104">Origini eventi</span><span class="sxs-lookup"><span data-stu-id="bdeda-104">Event Sources</span></span>

<span data-ttu-id="bdeda-105">Ogni log della [chiave EventLog](eventlog-key.md) contiene sottochiavi denominate *origini eventi*.</span><span class="sxs-lookup"><span data-stu-id="bdeda-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="bdeda-106">L'origine evento è il nome del software che registra l'evento.</span><span class="sxs-lookup"><span data-stu-id="bdeda-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="bdeda-107">Spesso è il nome dell'applicazione o il nome di un sottocomponente dell'applicazione, se l'applicazione è di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="bdeda-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="bdeda-108">È possibile aggiungere al registro di sistema un massimo di 16.384 origini evento.</span><span class="sxs-lookup"><span data-stu-id="bdeda-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="bdeda-109">Il registro di **sicurezza** è solo per uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="bdeda-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="bdeda-110">I driver di dispositivo devono aggiungere i nomi al registro di **sistema** .</span><span class="sxs-lookup"><span data-stu-id="bdeda-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="bdeda-111">Le applicazioni e i servizi devono aggiungere i nomi al registro **applicazioni** o creare un log personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bdeda-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="bdeda-112">La struttura delle origini evento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="bdeda-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="bdeda-113">Non è possibile usare un nome di origine già usato come nome di log.</span><span class="sxs-lookup"><span data-stu-id="bdeda-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="bdeda-114">Inoltre, i nomi di origine non possono essere gerarchici; ovvero non possono contenere il carattere barra rovesciata (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="bdeda-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="bdeda-115">Ogni origine evento contiene informazioni, ad esempio un [file di messaggio](message-files.md), specifiche del software che registrerà gli eventi, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bdeda-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bdeda-116">Valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="bdeda-116">Registry Value</span></span></th>
<th><span data-ttu-id="bdeda-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdeda-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bdeda-118"><strong>CategoryCount</strong></span><span class="sxs-lookup"><span data-stu-id="bdeda-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="bdeda-119">Numero di categorie di eventi supportate.</span><span class="sxs-lookup"><span data-stu-id="bdeda-119">Number of event categories supported.</span></span> <span data-ttu-id="bdeda-120">Questo valore è di tipo <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="bdeda-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdeda-121"><strong>CategoryMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="bdeda-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="bdeda-122">Percorso del file di messaggio di categoria.</span><span class="sxs-lookup"><span data-stu-id="bdeda-122">Path to the category message file.</span></span> <span data-ttu-id="bdeda-123">Un file di messaggio di categoria contiene stringhe dipendenti dalla lingua che descrivono le categorie.</span><span class="sxs-lookup"><span data-stu-id="bdeda-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="bdeda-124">Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="bdeda-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdeda-125"><strong>EventMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="bdeda-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="bdeda-126">Percorso di uno o più file di messaggio di evento; utilizzare un punto e virgola per delimitare più file.</span><span class="sxs-lookup"><span data-stu-id="bdeda-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="bdeda-127">Un file di messaggio di evento contiene stringhe dipendenti dalla lingua che descrivono gli eventi.</span><span class="sxs-lookup"><span data-stu-id="bdeda-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="bdeda-128">Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="bdeda-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdeda-129"><strong>ParameterMessageFile</strong></span><span class="sxs-lookup"><span data-stu-id="bdeda-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="bdeda-130">Percorso del file dei messaggi di parametro.</span><span class="sxs-lookup"><span data-stu-id="bdeda-130">Path to the parameter message file.</span></span> <span data-ttu-id="bdeda-131">Un file di messaggi di parametro contiene stringhe indipendenti dalla lingua da inserire nelle stringhe di descrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bdeda-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="bdeda-132">Questo valore può essere di tipo <strong>REG_SZ</strong> o <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="bdeda-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdeda-133"><strong>TypesSupported</strong></span><span class="sxs-lookup"><span data-stu-id="bdeda-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="bdeda-134">Maschera di maschera dei tipi supportati.</span><span class="sxs-lookup"><span data-stu-id="bdeda-134">Bitmask of supported types.</span></span> <span data-ttu-id="bdeda-135">Questo valore è di tipo <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="bdeda-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="bdeda-136">Può essere uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bdeda-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="bdeda-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span><span class="sxs-lookup"><span data-stu-id="bdeda-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="bdeda-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span><span class="sxs-lookup"><span data-stu-id="bdeda-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="bdeda-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span><span class="sxs-lookup"><span data-stu-id="bdeda-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="bdeda-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span><span class="sxs-lookup"><span data-stu-id="bdeda-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="bdeda-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span><span class="sxs-lookup"><span data-stu-id="bdeda-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bdeda-142">Quando un'applicazione usa la funzione [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) per ottenere un handle per un log eventi, il servizio di registrazione eventi cerca l'origine eventi specificata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bdeda-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="bdeda-143">Ad esempio, il registro **applicazioni** potrebbe contenere origini eventi per Microsoft SQL Server e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bdeda-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="bdeda-144">Se un'applicazione utilizza [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) o **OpenEventLog** con il nome di origine dell'applicazione, SQL o Excel, il servizio di registrazione eventi restituisce un handle al registro **applicazioni** .</span><span class="sxs-lookup"><span data-stu-id="bdeda-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="bdeda-145">Un'applicazione può usare il registro **applicazioni** senza aggiungere una nuova origine evento al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="bdeda-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="bdeda-146">Se l'applicazione chiama [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) e passa un nome di origine che non è possibile trovare nel registro di sistema, per impostazione predefinita il servizio di registrazione eventi usa il registro **applicazioni** .</span><span class="sxs-lookup"><span data-stu-id="bdeda-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="bdeda-147">Tuttavia, poiché non sono presenti file di messaggi, il Visualizzatore eventi non è in grado di eseguire il mapping di qualsiasi identificatore di evento o categoria di eventi a una stringa di descrizione e verrà visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="bdeda-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="bdeda-148">Per questo motivo, è necessario aggiungere un'origine evento univoca al registro di sistema per l'applicazione e specificare un file di messaggio.</span><span class="sxs-lookup"><span data-stu-id="bdeda-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 



