---
description: Gli identificatori di evento identificano in modo univoco un particolare evento.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificatori evento (registrazione eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527271"
---
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="262e0-103">Identificatori evento (registrazione eventi)</span><span class="sxs-lookup"><span data-stu-id="262e0-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="262e0-104">Gli identificatori di evento identificano in modo univoco un particolare evento.</span><span class="sxs-lookup"><span data-stu-id="262e0-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="262e0-105">Ogni [origine evento](event-sources.md) può definire i propri eventi numerati e le stringhe di descrizione alle quali viene eseguito il mapping nel file di messaggio.</span><span class="sxs-lookup"><span data-stu-id="262e0-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="262e0-106">I visualizzatori eventi possono presentare queste stringhe all'utente.</span><span class="sxs-lookup"><span data-stu-id="262e0-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="262e0-107">Dovrebbero aiutare l'utente a capire cosa si è verificato un errore e suggerire quali azioni eseguire.</span><span class="sxs-lookup"><span data-stu-id="262e0-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="262e0-108">Indirizzare la descrizione agli utenti che risolve i propri problemi, non agli amministratori o ai tecnici del supporto.</span><span class="sxs-lookup"><span data-stu-id="262e0-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="262e0-109">Per ulteriori informazioni, vedere [linee guida](/windows/desktop/Debug/error-message-guidelines)per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="262e0-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="262e0-110">Formato</span><span class="sxs-lookup"><span data-stu-id="262e0-110">Format</span></span>

<span data-ttu-id="262e0-111">Il diagramma seguente illustra il formato di un identificatore di evento.</span><span class="sxs-lookup"><span data-stu-id="262e0-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="262e0-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Gravità</span><span class="sxs-lookup"><span data-stu-id="262e0-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="262e0-113">Gravità.</span><span class="sxs-lookup"><span data-stu-id="262e0-113">Severity.</span></span> <span data-ttu-id="262e0-114">Il livello di gravità viene definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="262e0-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="262e0-115">00-operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="262e0-115">00 - Success</span></span></dd> <dd><span data-ttu-id="262e0-116">01-informativo</span><span class="sxs-lookup"><span data-stu-id="262e0-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="262e0-117">10-avviso</span><span class="sxs-lookup"><span data-stu-id="262e0-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="262e0-118">11-errore</span><span class="sxs-lookup"><span data-stu-id="262e0-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="262e0-119"><span id="C"></span><span id="c"></span>C</span><span class="sxs-lookup"><span data-stu-id="262e0-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="262e0-120">Bit del cliente.</span><span class="sxs-lookup"><span data-stu-id="262e0-120">Customer bit.</span></span> <span data-ttu-id="262e0-121">Questo bit è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="262e0-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="262e0-122">0-codice di sistema</span><span class="sxs-lookup"><span data-stu-id="262e0-122">0 - System code</span></span></dd> <dd><span data-ttu-id="262e0-123">1-codice cliente</span><span class="sxs-lookup"><span data-stu-id="262e0-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="262e0-124"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="262e0-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="262e0-125">Bit riservati.</span><span class="sxs-lookup"><span data-stu-id="262e0-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="262e0-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Struttura</span><span class="sxs-lookup"><span data-stu-id="262e0-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="262e0-127">Codice della struttura.</span><span class="sxs-lookup"><span data-stu-id="262e0-127">Facility code.</span></span> <span data-ttu-id="262e0-128">Questo valore può essere null per la funzionalità \_ .</span><span class="sxs-lookup"><span data-stu-id="262e0-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="262e0-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice</span><span class="sxs-lookup"><span data-stu-id="262e0-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="262e0-130">Codice di stato per la struttura.</span><span class="sxs-lookup"><span data-stu-id="262e0-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="262e0-131">Definizioni dei messaggi</span><span class="sxs-lookup"><span data-stu-id="262e0-131">Message Definitions</span></span>

<span data-ttu-id="262e0-132">I messaggi vengono definiti nel file di messaggio dell'evento.</span><span class="sxs-lookup"><span data-stu-id="262e0-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="262e0-133">Le stringhe di descrizione nel file dei messaggi di evento vengono indicizzate in base all'identificatore dell'evento, consentendo Visualizzatore eventi di visualizzare il testo specifico dell'evento per qualsiasi evento in base all'identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="262e0-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="262e0-134">Tutte le descrizioni sono localizzate e dipendenti dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="262e0-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="262e0-135">Per ulteriori informazioni sulla compilazione di un file di messaggio, vedere [file di testo del messaggio](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="262e0-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="262e0-136">Le stringhe di descrizione possono contenere segnaposto di stringa di inserimento, nel formato%*n*, dove %1 indica la prima stringa di inserimento e così via.</span><span class="sxs-lookup"><span data-stu-id="262e0-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="262e0-137">Ad esempio, di seguito è riportata una voce di esempio nel file con estensione MC:</span><span class="sxs-lookup"><span data-stu-id="262e0-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="262e0-138">In questo caso, il buffer restituito da [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contiene stringhe di inserimento.</span><span class="sxs-lookup"><span data-stu-id="262e0-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="262e0-139">Il membro **NumStrings** della struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica il numero di stringhe di inserimento.</span><span class="sxs-lookup"><span data-stu-id="262e0-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="262e0-140">Il membro **StringOffset** della struttura **EVENTLOGRECORD** indica la posizione della prima stringa di inserimento nel buffer.</span><span class="sxs-lookup"><span data-stu-id="262e0-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="262e0-141">È possibile passare una matrice di \_ PTRS DWORD che puntano all'indirizzo ogni stringa nel buffer quando si chiama la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e le stringhe vengono inserite nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="262e0-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="262e0-142">La stringa di descrizione può inoltre contenere segnaposto per le stringhe di parametri del file di messaggio dei parametri.</span><span class="sxs-lookup"><span data-stu-id="262e0-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="262e0-143">Il formato dei segnaposto è%%*n*, dove% %1 viene sostituito dalla stringa del parametro con l'identificatore 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="262e0-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="262e0-144">Tuttavia, spetta all'utente inserire le stringhe dei parametri nella stringa di messaggio restituita da [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="262e0-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="262e0-145">In genere, si chiama **FormatMessage** per ottenere la stringa di messaggio per l'evento.</span><span class="sxs-lookup"><span data-stu-id="262e0-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="262e0-146">Viene quindi analizzata la stringa di messaggio per%%*n* parametri.</span><span class="sxs-lookup"><span data-stu-id="262e0-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="262e0-147">Se il messaggio contiene uno o più parametri, caricare il valore del registro di sistema **ParameterMessageFile** per l'origine.</span><span class="sxs-lookup"><span data-stu-id="262e0-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="262e0-148">Per ogni parametro nella stringa del messaggio, ottenere l'identificatore e passarlo a **FormatMessage** per ottenere la stringa di parametro.</span><span class="sxs-lookup"><span data-stu-id="262e0-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="262e0-149">Sostituire il parametro nella stringa del messaggio con la stringa di parametro restituita da **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="262e0-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="262e0-150">Stringhe di inserimento</span><span class="sxs-lookup"><span data-stu-id="262e0-150">Insertion Strings</span></span>

<span data-ttu-id="262e0-151">Le stringhe di inserimento sono stringhe indipendenti dal linguaggio facoltative utilizzate per inserire i valori per i segnaposto nelle stringhe di descrizione.</span><span class="sxs-lookup"><span data-stu-id="262e0-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="262e0-152">Poiché le stringhe non sono localizzate, è fondamentale che questi segnaposto vengano utilizzati solo per rappresentare stringhe indipendenti dalla lingua, ad esempio valori numerici, nomi file, nomi utente e così via.</span><span class="sxs-lookup"><span data-stu-id="262e0-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="262e0-153">La lunghezza della stringa non deve superare 32 kilobyte-1 caratteri.</span><span class="sxs-lookup"><span data-stu-id="262e0-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="262e0-154">Evitare di usare più stringhe per creare una descrizione più ampia.</span><span class="sxs-lookup"><span data-stu-id="262e0-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="262e0-155">Una stringa di inserimento deve essere considerata come dati, non come testo.</span><span class="sxs-lookup"><span data-stu-id="262e0-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="262e0-156">Nell'esempio seguente, ad esempio, pszString1 e pszString2 non devono essere usati come stringhe di inserimento per pszDescription.</span><span class="sxs-lookup"><span data-stu-id="262e0-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="262e0-157">Nell'esempio seguente è opportuno usare pszString1 o pszString2 per la stringa di inserimento in pszDescription.</span><span class="sxs-lookup"><span data-stu-id="262e0-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
