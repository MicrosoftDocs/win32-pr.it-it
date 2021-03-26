---
description: Di seguito sono elencate le procedure consigliate da utilizzare quando si utilizzano le associazioni di file.
title: Procedure consigliate per le associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525795"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="7f67a-103">Procedure consigliate per le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-103">Best Practices for File Associations</span></span>

<span data-ttu-id="7f67a-104">Di seguito sono elencate le procedure consigliate da utilizzare quando si utilizzano le associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="7f67a-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="7f67a-105">Non copiare le associazioni di file dal registro di sistema</span><span class="sxs-lookup"><span data-stu-id="7f67a-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="7f67a-106">Evitare Hard-Coding percorsi nel registro di sistema laddove possibile</span><span class="sxs-lookup"><span data-stu-id="7f67a-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="7f67a-107">Racchiudere sempre le stringhe in espansione tra virgolette</span><span class="sxs-lookup"><span data-stu-id="7f67a-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="7f67a-108">Non confondere AutoPlay/autorun con le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="7f67a-109">Non confondere il database MIME di Internet Explorer con le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="7f67a-110">Usare ProgID correttamente formattati e con versione</span><span class="sxs-lookup"><span data-stu-id="7f67a-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="7f67a-111">Non usare estensioni di file brevi</span><span class="sxs-lookup"><span data-stu-id="7f67a-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="7f67a-112">Registrare nuovi tipi di file nel database MIME IANA</span><span class="sxs-lookup"><span data-stu-id="7f67a-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="7f67a-113">Iscriversi con il servizio Web Windows per le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="7f67a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f67a-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="7f67a-115">Non copiare le associazioni di file dal registro di sistema</span><span class="sxs-lookup"><span data-stu-id="7f67a-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="7f67a-116">Si consiglia di non copiare le associazioni di file esistenti dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7f67a-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="7f67a-117">Questo comporta spesso la propagazione di associazioni di file in formato non corretto.</span><span class="sxs-lookup"><span data-stu-id="7f67a-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="7f67a-118">Al contrario, è necessario seguire i passaggi descritti in [scenario di esempio di associazione di file](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="7f67a-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="7f67a-119">Evitare Hard-Coding percorsi nel registro di sistema laddove possibile</span><span class="sxs-lookup"><span data-stu-id="7f67a-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="7f67a-120">Analogamente a quanto i percorsi di programmazione dei programmi possono causare problemi, i percorsi hardcoded nel registro di sistema possono causare anche problemi.</span><span class="sxs-lookup"><span data-stu-id="7f67a-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="7f67a-121">È invece consigliabile utilizzare le stringhe di espansione del registro di sistema (REG \_ expand \_ SZ) per fornire l'indipendenza del percorso ove applicabile.</span><span class="sxs-lookup"><span data-stu-id="7f67a-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="7f67a-122">Ad esempio, invece di usare questo metodo:</span><span class="sxs-lookup"><span data-stu-id="7f67a-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="7f67a-123">Usare questo metodo:</span><span class="sxs-lookup"><span data-stu-id="7f67a-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="7f67a-124">Racchiudere sempre le stringhe in espansione tra virgolette</span><span class="sxs-lookup"><span data-stu-id="7f67a-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="7f67a-125">Le stringhe di espansione possono contenere spazi quando si espandono.</span><span class="sxs-lookup"><span data-stu-id="7f67a-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="7f67a-126">Poiché gli spazi vengono spesso interpretati come delimitatori di argomento, causano problemi in determinate circostanze.</span><span class="sxs-lookup"><span data-stu-id="7f67a-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="7f67a-127">Ad esempio, un comando per richiamare il programma può essere archiviato nel registro di sistema come segue:</span><span class="sxs-lookup"><span data-stu-id="7f67a-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="7f67a-128">In programma si prevede che %1 sia il percorso completo di un nome file e %2 è un'opzione per indicare un'azione.</span><span class="sxs-lookup"><span data-stu-id="7f67a-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="7f67a-129">Se questo comando viene eseguito con gli argomenti **c: \\ Program Files \\ \\document.txt** e **/Print** e supponendo una SystemRoot di c: \\ WinNT, si espande a:</span><span class="sxs-lookup"><span data-stu-id="7f67a-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="7f67a-130">In questo caso, il programma indica che il primo argomento è C: \\ Program e il secondo argomento è file \\ My, che non è il comportamento previsto.</span><span class="sxs-lookup"><span data-stu-id="7f67a-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="7f67a-131">Gli argomenti vengono interpretati correttamente, tuttavia, indipendentemente dal fatto che contengano spazi, se le stringhe in espansione sono racchiuse tra virgolette come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="7f67a-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="7f67a-132">Non confondere AutoPlay/autorun con le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="7f67a-133">Le associazioni di file sono simili a AutoPlay/autorun in alcuni modi.</span><span class="sxs-lookup"><span data-stu-id="7f67a-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="7f67a-134">Tuttavia, AutoPlay/autorun offre funzionalità separate e distinte da quelle fornite dalle associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="7f67a-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="7f67a-135">Per altre informazioni, vedere [creazione di un'applicazione CD-ROM abilitata per l'esecuzione automatica](autoplay.md).</span><span class="sxs-lookup"><span data-stu-id="7f67a-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="7f67a-136">Non confondere il database MIME di Internet Explorer con le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="7f67a-137">Le associazioni di file sono simili al database MIME di Windows Internet Explorer, in quanto i tipi di file possono (e dovrebbero) includere una definizione di tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="7f67a-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="7f67a-138">Tuttavia, il database MIME di Internet Explorer è separato e distinto dalle associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="7f67a-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="7f67a-139">Usare ProgID correttamente formattati e con versione</span><span class="sxs-lookup"><span data-stu-id="7f67a-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="7f67a-140">Usare sempre [ProgID con versione](fa-progids.md), anche se è presente una sola versione del ProgID.</span><span class="sxs-lookup"><span data-stu-id="7f67a-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="7f67a-141">I ProgID con versione consentono di evitare conflitti e sovrascritture ProgID.</span><span class="sxs-lookup"><span data-stu-id="7f67a-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="7f67a-142">Consentono inoltre di coesistere versioni diverse di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f67a-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="7f67a-143">Non usare estensioni di file brevi</span><span class="sxs-lookup"><span data-stu-id="7f67a-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="7f67a-144">Le estensioni dei nomi di file lunghi offrono i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f67a-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="7f67a-145">La lunghezza limitata delle estensioni brevi le rende soggette a *collisioni di estensione.*</span><span class="sxs-lookup"><span data-stu-id="7f67a-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="7f67a-146">Una collisione di estensione si verifica quando viene usata la stessa estensione per classificare più tipi di file.</span><span class="sxs-lookup"><span data-stu-id="7f67a-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="7f67a-147">L'utilizzo di estensioni lunghe comporta una riduzione significativa delle probabilità che si verifichi un conflitto.</span><span class="sxs-lookup"><span data-stu-id="7f67a-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="7f67a-148">I nomi di file brevi tendono a essere piuttosto criptici.</span><span class="sxs-lookup"><span data-stu-id="7f67a-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="7f67a-149">Le estensioni lunghe tendono a essere più significative perché è possibile incorporare informazioni aggiuntive nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7f67a-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="7f67a-150">Per ulteriori informazioni, vedere [estensioni di file](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="7f67a-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="7f67a-151">Registrare nuovi tipi di file nel database MIME IANA</span><span class="sxs-lookup"><span data-stu-id="7f67a-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="7f67a-152">IANA (Internet Assigned Numbers Authority) mantiene un database pubblico di tipi MIME registrati.</span><span class="sxs-lookup"><span data-stu-id="7f67a-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="7f67a-153">Quando si definisce un nuovo tipo di file pubblico, è consigliabile definire anche un tipo MIME per il tipo di file e registrare questo tipo con IANA.</span><span class="sxs-lookup"><span data-stu-id="7f67a-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="7f67a-154">Non è previsto alcun costo per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="7f67a-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="7f67a-155">Iscriversi con il servizio Web Windows per le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="7f67a-156">Gli sviluppatori di applicazioni possono iscriversi al servizio Web Windows usato dagli utenti per trovare applicazioni che possono operare su tipi di file specifici.</span><span class="sxs-lookup"><span data-stu-id="7f67a-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="7f67a-157">Il processo per l'iscrizione al servizio Web è descritto in dettaglio nel [processo di onboarding del sistema di associazione file di Windows](https://support.microsoft.com/kb/929149).</span><span class="sxs-lookup"><span data-stu-id="7f67a-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f67a-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f67a-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f67a-159">Scenario di esempio di associazione di file</span><span class="sxs-lookup"><span data-stu-id="7f67a-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="7f67a-160">Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="7f67a-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="7f67a-161">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="7f67a-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="7f67a-162">Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)</span><span class="sxs-lookup"><span data-stu-id="7f67a-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 



