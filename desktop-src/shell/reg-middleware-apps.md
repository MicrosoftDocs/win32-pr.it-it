---
description: 'In questo argomento viene illustrato come registrare un programma nel registro di sistema di Windows come uno dei seguenti tipi di client: browser, posta elettronica, riproduzione multimediale, messaggistica immediata o macchina virtuale per Java.'
title: Registrazione di programmi con tipi di client
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886041"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="f92d0-103">Registrazione di programmi con tipi di client</span><span class="sxs-lookup"><span data-stu-id="f92d0-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="f92d0-104">In questo argomento viene illustrato come registrare un programma nel registro di sistema di Windows come uno dei seguenti tipi di client: browser, posta elettronica, riproduzione multimediale, messaggistica immediata o macchina virtuale per Java.</span><span class="sxs-lookup"><span data-stu-id="f92d0-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-105">Queste informazioni si applicano ai sistemi operativi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f92d0-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="f92d0-106">Windows 2000 Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="f92d0-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="f92d0-107">Windows 2000 Service Pack 4 (SP4)</span><span class="sxs-lookup"><span data-stu-id="f92d0-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="f92d0-108">Windows XP Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f92d0-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="f92d0-109">Windows XP Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="f92d0-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="f92d0-110">Windows XP Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="f92d0-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="f92d0-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f92d0-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="f92d0-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f92d0-112">Windows Vista</span></span>
> -   <span data-ttu-id="f92d0-113">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="f92d0-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="f92d0-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f92d0-114">Windows 8</span></span>

 

<span data-ttu-id="f92d0-115">In questo argomento sono incluse le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="f92d0-116">Elementi di registrazione comuni per tutti i tipi di client</span><span class="sxs-lookup"><span data-stu-id="f92d0-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="f92d0-117">Selezione di un nome canonico</span><span class="sxs-lookup"><span data-stu-id="f92d0-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="f92d0-118">Registrazione del nome visualizzato di un programma</span><span class="sxs-lookup"><span data-stu-id="f92d0-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="f92d0-119">Registrazione dell'icona di un programma</span><span class="sxs-lookup"><span data-stu-id="f92d0-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="f92d0-120">Registrazione di un verbo aperto</span><span class="sxs-lookup"><span data-stu-id="f92d0-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="f92d0-121">Registrazione delle informazioni di installazione</span><span class="sxs-lookup"><span data-stu-id="f92d0-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="f92d0-122">Elementi di registrazione per tipi client specifici</span><span class="sxs-lookup"><span data-stu-id="f92d0-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="f92d0-123">Registrazione del menu Start</span><span class="sxs-lookup"><span data-stu-id="f92d0-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="f92d0-124">Registrazione client di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="f92d0-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="f92d0-125">Completa registrazioni di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="f92d0-126">Un browser di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="f92d0-127">Un browser di posta elettronica di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="f92d0-128">Media Player di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="f92d0-129">Programma Instant Messenger di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="f92d0-130">Una macchina virtuale di esempio per Java</span><span class="sxs-lookup"><span data-stu-id="f92d0-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="f92d0-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f92d0-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="f92d0-132">In questo argomento viene estesa la documentazione esistente sulla registrazione di un programma come tipo di client specifico.</span><span class="sxs-lookup"><span data-stu-id="f92d0-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="f92d0-133">Per i collegamenti alla documentazione, vedere la sezione Argomenti correlati.</span><span class="sxs-lookup"><span data-stu-id="f92d0-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="f92d0-134">Elementi di registrazione comuni per tutti i tipi di client</span><span class="sxs-lookup"><span data-stu-id="f92d0-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="f92d0-135">Quando si registra un programma come tipo di client, la maggior parte delle voci del registro di sistema sono le stesse indipendentemente dal tipo di client.</span><span class="sxs-lookup"><span data-stu-id="f92d0-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="f92d0-136">Alcune voci del registro di sistema, tuttavia, sono specifiche del tipo di client e sono indicate nella sezione [elementi di registrazione per tipi di client specifici](#registration-elements-for-specific-client-types) .</span><span class="sxs-lookup"><span data-stu-id="f92d0-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="f92d0-137">In questa sezione vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f92d0-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="f92d0-138">Selezione di un nome canonico</span><span class="sxs-lookup"><span data-stu-id="f92d0-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="f92d0-139">Registrazione del nome visualizzato di un programma</span><span class="sxs-lookup"><span data-stu-id="f92d0-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="f92d0-140">Registrazione dell'icona di un programma</span><span class="sxs-lookup"><span data-stu-id="f92d0-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="f92d0-141">Registrazione di un verbo aperto</span><span class="sxs-lookup"><span data-stu-id="f92d0-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="f92d0-142">Registrazione delle informazioni di installazione</span><span class="sxs-lookup"><span data-stu-id="f92d0-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="f92d0-143">I nomi delle sottochiavi indicati in corsivo in questo argomento sono segnaposto per i nomi di sottochiavi definiti dall'utente o per un set di valori possibili.</span><span class="sxs-lookup"><span data-stu-id="f92d0-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="f92d0-144">Gli esempi completi con i nomi di esempio sono disponibili nella sezione [completa registrazioni di esempio](#complete-sample-registrations) .</span><span class="sxs-lookup"><span data-stu-id="f92d0-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="f92d0-145">Tutte le informazioni di registrazione del tipo di client vengono archiviate con la sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="f92d0-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="f92d0-146">*ClientTypeName* è uno dei seguenti nomi di sottochiavi:</span><span class="sxs-lookup"><span data-stu-id="f92d0-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="f92d0-147">StartMenuInternet (per i browser)</span><span class="sxs-lookup"><span data-stu-id="f92d0-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="f92d0-148">Posta elettronica (per la posta elettronica)</span><span class="sxs-lookup"><span data-stu-id="f92d0-148">Mail (for email)</span></span>
-   <span data-ttu-id="f92d0-149">Supporti (per la riproduzione di contenuti multimediali)</span><span class="sxs-lookup"><span data-stu-id="f92d0-149">Media (for media playback)</span></span>
-   <span data-ttu-id="f92d0-150">Messaggistica immediata (per la messaggistica istantanea)</span><span class="sxs-lookup"><span data-stu-id="f92d0-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="f92d0-151">JavaVM (per la macchina virtuale per Java)</span><span class="sxs-lookup"><span data-stu-id="f92d0-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="f92d0-152">In questo argomento si noteranno i riferimenti a un programma per computer fittizio denominato "Lit View" di Litware Inc., con un file eseguibile denominato Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="f92d0-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="f92d0-153">Questo ipotetico programma viene usato in modo intercambiabile come Instant Messenger, browser o un altro tipo di programma client, in base alle esigenze a scopo illustrativo.</span><span class="sxs-lookup"><span data-stu-id="f92d0-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="f92d0-154">Selezione di un nome canonico</span><span class="sxs-lookup"><span data-stu-id="f92d0-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="f92d0-155">Il fornitore deve scegliere un *nome canonico* per il programma.</span><span class="sxs-lookup"><span data-stu-id="f92d0-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="f92d0-156">Il nome canonico non viene mai visualizzato all'utente, pertanto non è necessario localizzarlo.</span><span class="sxs-lookup"><span data-stu-id="f92d0-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="f92d0-157">Il suo unico scopo è fornire una stringa univoca che può essere usata per identificare il programma.</span><span class="sxs-lookup"><span data-stu-id="f92d0-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="f92d0-158">Corrisponde in genere al nome in lingua inglese del programma, ma si tratta semplicemente di una convenzione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="f92d0-159">Per i tipi di client diversi dai browser, il nome canonico può essere una stringa qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="f92d0-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="f92d0-160">Scegliere un nome univoco, che probabilmente non verrà usato da un altro fornitore.</span><span class="sxs-lookup"><span data-stu-id="f92d0-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="f92d0-161">Per i client del browser, il nome canonico deve essere il nome, inclusa l'estensione, del file eseguibile associato. ad esempio, "Litview.exe".</span><span class="sxs-lookup"><span data-stu-id="f92d0-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="f92d0-162">Di seguito sono riportati alcuni esempi di nomi canonici.</span><span class="sxs-lookup"><span data-stu-id="f92d0-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="f92d0-163">Iexplore.exe (browser)</span><span class="sxs-lookup"><span data-stu-id="f92d0-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="f92d0-164">Windows Mail (posta elettronica)</span><span class="sxs-lookup"><span data-stu-id="f92d0-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="f92d0-165">Media Player Windows (supporto)</span><span class="sxs-lookup"><span data-stu-id="f92d0-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="f92d0-166">Windows Messenger (messaggistica istantanea)</span><span class="sxs-lookup"><span data-stu-id="f92d0-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="f92d0-167">Registrare il nome canonico creando una sottochiave come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="f92d0-168">Il nome della sottochiave è il nome canonico.</span><span class="sxs-lookup"><span data-stu-id="f92d0-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="f92d0-169">Tutte le informazioni relative alla registrazione di tale programma sono disponibili in questa sottochiave.</span><span class="sxs-lookup"><span data-stu-id="f92d0-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="f92d0-170">Registrazione del nome visualizzato di un programma</span><span class="sxs-lookup"><span data-stu-id="f92d0-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="f92d0-171">Il passaggio successivo della registrazione consiste nel specificare il nome visualizzato del programma.</span><span class="sxs-lookup"><span data-stu-id="f92d0-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="f92d0-172">Viene specificato come valore sotto la chiave del nome canonico, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="f92d0-173">Si noti che *CanonicalName* e *ClientTypeName* non sono i nomi effettivi delle chiavi, ma solo i segnaposto per i nomi veri, ad esempio la *visualizzazione illuminata*.</span><span class="sxs-lookup"><span data-stu-id="f92d0-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-174">A partire da Windows 8, il nome usato per registrare l' [accesso al programma set e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md) e per i [programmi predefiniti](default-programs.md) deve corrispondere affinché le modifiche apportate da SPAD per attivare le registrazioni dei programmi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="f92d0-175">Il valore **LocalizedString** è una \_ stringa reg SZ ed è costituito da un segno di chiocciola (@), dal percorso completo di un file con estensione dll o exe, da una virgola, da un segno meno e da un numero intero decimale.</span><span class="sxs-lookup"><span data-stu-id="f92d0-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="f92d0-176">Il numero intero decimale è l'ID di una risorsa di tipo stringa, contenuto all'interno del file con estensione dll o exe, il cui valore deve essere visualizzato all'utente come nome del client.</span><span class="sxs-lookup"><span data-stu-id="f92d0-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="f92d0-177">Si noti che il percorso del file non richiede virgolette, anche se contiene spazi.</span><span class="sxs-lookup"><span data-stu-id="f92d0-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="f92d0-178">La registrazione della stringa del nome visualizzato in questo modo consente di usare la stessa registrazione per più lingue.</span><span class="sxs-lookup"><span data-stu-id="f92d0-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="f92d0-179">Ogni installazione della lingua fornisce un file di risorse diverso con il nome visualizzato archiviato con lo stesso ID di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f92d0-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="f92d0-180">Nell'esempio riportato di seguito viene illustrata la registrazione di un programma di messaggistica istantanea di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="f92d0-181">Poiché si tratta di un programma di messaggistica immediata, la sottochiave *CanonicalName* (in questo caso la *visualizzazione illuminata*) viene archiviata nella sottochiave **im** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="f92d0-182">Si noti l'uso della voce (impostazione predefinita) come dichiarazione secondaria del nome visualizzato del client.</span><span class="sxs-lookup"><span data-stu-id="f92d0-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="f92d0-183">Se **LocalizedString** non è presente, viene invece utilizzato il valore (predefinito).</span><span class="sxs-lookup"><span data-stu-id="f92d0-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="f92d0-184">Funziona con tutti i tipi di client (browser Internet, browser di posta elettronica, messaggeri istantanei e lettori multimediali).</span><span class="sxs-lookup"><span data-stu-id="f92d0-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="f92d0-185">Per garantire la compatibilità con il [layout del registro di sistema del client di Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), i programmi di posta elettronica devono impostare il valore (predefinito) della sottochiave *CanonicalName* sul nome visualizzato del client nella lingua attualmente installata.</span><span class="sxs-lookup"><span data-stu-id="f92d0-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="f92d0-186">Registrazione dell'icona di un programma</span><span class="sxs-lookup"><span data-stu-id="f92d0-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-187">Questa sezione non si applica a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f92d0-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="f92d0-188">Per impostazione predefinita, la sezione superiore del menu **Start** di Windows XP e Windows Vista contiene le icone **Internet** e **posta elettronica** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="f92d0-189">Queste icone non sono presenti in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f92d0-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="f92d0-190">Per i client del browser e della posta elettronica, quando un programma viene assegnato come valore predefinito per il tipo di client, viene visualizzata l'icona registrata del programma per le voci del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="f92d0-191">La registrazione dell'icona di un programma è obbligatoria per i client del browser e della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f92d0-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="f92d0-192">La registrazione di un'icona per la riproduzione multimediale, la messaggistica immediata o la macchina virtuale per i tipi di client Java è facoltativa e le icone registrate per tali tipi di client non sono attualmente utilizzate da Windows e non vengono visualizzate nella sezione superiore dei menu di **avvio** di Windows XP o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f92d0-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="f92d0-193">Per registrare un'icona per un programma client, aggiungere una sottochiave **DefaultIcon** con un valore predefinito, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="f92d0-194">Il valore **filePath** è il percorso completo del file che contiene l'icona.</span><span class="sxs-lookup"><span data-stu-id="f92d0-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="f92d0-195">Questo percorso non richiede virgolette, anche se contiene spazi.</span><span class="sxs-lookup"><span data-stu-id="f92d0-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="f92d0-196">Il valore **IconIndex** viene interpretato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f92d0-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="f92d0-197">Se **IconIndex** è un numero positivo, il numero viene usato come indice della matrice in *base zero* delle icone archiviate nel file.</span><span class="sxs-lookup"><span data-stu-id="f92d0-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="f92d0-198">Se, ad esempio, **IconIndex** è 1, la seconda icona viene caricata dal file.</span><span class="sxs-lookup"><span data-stu-id="f92d0-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="f92d0-199">Se **IconIndex** è un numero negativo, il valore assoluto di **IconIndex** viene usato come identificatore di risorsa (anziché come indice) per l'icona.</span><span class="sxs-lookup"><span data-stu-id="f92d0-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="f92d0-200">Ad esempio, se **IconIndex** è-3, l'icona con l'identificatore di risorsa 3 viene caricata dal file.</span><span class="sxs-lookup"><span data-stu-id="f92d0-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="f92d0-201">Nell'esempio seguente viene illustrata la registrazione di un ipotetico browser di visualizzazione illuminato.</span><span class="sxs-lookup"><span data-stu-id="f92d0-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="f92d0-202">La seconda icona archiviata nel file di Litview.exe viene utilizzata come impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f92d0-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="f92d0-203">Registrazione di un verbo aperto</span><span class="sxs-lookup"><span data-stu-id="f92d0-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-204">Questa sezione non si applica a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f92d0-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="f92d0-205">Il passaggio seguente è necessario solo per i client di posta elettronica e browser.</span><span class="sxs-lookup"><span data-stu-id="f92d0-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="f92d0-206">Si supponga che un utente abbia selezionato il programma come Internet o programma di posta elettronica predefinito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="f92d0-207">Tale utente fa clic sull'icona **Internet** o **posta elettronica** nel menu **Start** di Windows XP o Windows Vista per aprire il programma.</span><span class="sxs-lookup"><span data-stu-id="f92d0-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="f92d0-208">A questo punto, viene eseguita la riga di comando registrata come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="f92d0-209">La riga di comando deve specificare un percorso assoluto completo del file, seguito da opzioni facoltative della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f92d0-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="f92d0-210">Se il tipo di voce è REG \_ expand \_ SZ, le variabili di ambiente possono essere usate nel percorso.</span><span class="sxs-lookup"><span data-stu-id="f92d0-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="f92d0-211">Utilizzare le virgolette appropriate per assicurarsi che gli spazi nella riga di comando non vengano interpretati erroneamente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="f92d0-212">La riga di comando deve eseguire il programma con le impostazioni predefinite appropriate.</span><span class="sxs-lookup"><span data-stu-id="f92d0-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="f92d0-213">Per impostazione predefinita, i browser vengono generalmente predefiniti per l'home page dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="f92d0-214">I programmi di posta elettronica aprono generalmente la **posta in arrivo** dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="f92d0-215">Nell'esempio seguente viene illustrata la registrazione di un `open` verbo per un browser di visualizzazione illuminato ipotetico.</span><span class="sxs-lookup"><span data-stu-id="f92d0-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="f92d0-216">Non specifica alcuna opzione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f92d0-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="f92d0-217">Si noti che in questo valore le virgolette vengono posizionate intorno al tracciato perché contiene spazi incorporati.</span><span class="sxs-lookup"><span data-stu-id="f92d0-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="f92d0-218">Se si ometteno queste virgolette, la riga di comando potrebbe essere interpretata erroneamente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="f92d0-219">Registrazione delle informazioni di installazione</span><span class="sxs-lookup"><span data-stu-id="f92d0-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-220">Questa sezione non si applica a Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f92d0-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="f92d0-221">Comando reinstalla</span><span class="sxs-lookup"><span data-stu-id="f92d0-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="f92d0-222">Comando Nascondi icone</span><span class="sxs-lookup"><span data-stu-id="f92d0-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="f92d0-223">Comando Mostra icone</span><span class="sxs-lookup"><span data-stu-id="f92d0-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="f92d0-224">Configurazione del programma di gruppo</span><span class="sxs-lookup"><span data-stu-id="f92d0-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="f92d0-225">Esempio di registrazione del browser</span><span class="sxs-lookup"><span data-stu-id="f92d0-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="f92d0-226">La funzionalità con cui l'utente seleziona programmi predefiniti per computer viene denominata e accessibile come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="f92d0-227">In Windows Vista è stata introdotta una nuova funzionalità, che consente di **impostare i programmi predefiniti** in base ai quali un utente può impostare le impostazioni predefinite per utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f92d0-228">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f92d0-228">Operating System</span></span></th>
<th><span data-ttu-id="f92d0-229">Titolo</span><span class="sxs-lookup"><span data-stu-id="f92d0-229">Title</span></span></th>
<th><span data-ttu-id="f92d0-230">Percorso di accesso</span><span class="sxs-lookup"><span data-stu-id="f92d0-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f92d0-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f92d0-231">Windows 7</span></span></td>
<td><span data-ttu-id="f92d0-232">Impostare l'accesso al programma e le impostazioni predefinite del computer</span><span class="sxs-lookup"><span data-stu-id="f92d0-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="f92d0-233">Opzione <strong>programmi predefiniti</strong> menu <strong>Start</strong></span><span class="sxs-lookup"><span data-stu-id="f92d0-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="f92d0-234"><strong>Programmi predefiniti</strong> Elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="f92d0-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f92d0-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f92d0-235">Windows Vista</span></span></td>
<td><span data-ttu-id="f92d0-236">Impostare l'accesso al programma e le impostazioni predefinite del computer</span><span class="sxs-lookup"><span data-stu-id="f92d0-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="f92d0-237">Opzione <strong>programmi predefiniti</strong> menu <strong>Start</strong></span><span class="sxs-lookup"><span data-stu-id="f92d0-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="f92d0-238"><strong>Programmi predefiniti</strong> Elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="f92d0-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f92d0-239">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="f92d0-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="f92d0-240">Impostare l'accesso al programma e le impostazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="f92d0-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="f92d0-241">Menu <strong>Start</strong></span><span class="sxs-lookup"><span data-stu-id="f92d0-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="f92d0-242"><strong>Installazione applicazioni</strong> Elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="f92d0-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f92d0-243">Windows XP SP1</span><span class="sxs-lookup"><span data-stu-id="f92d0-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="f92d0-244">Configura programmi</span><span class="sxs-lookup"><span data-stu-id="f92d0-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="f92d0-245"><strong>Installazione applicazioni</strong> Elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="f92d0-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f92d0-246">Per semplicità, in questo argomento viene usato il titolo di Windows 7 della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f92d0-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="f92d0-247">Tutte le versioni della funzionalità sono comunemente denominate SPAD.</span><span class="sxs-lookup"><span data-stu-id="f92d0-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-248">Se si esegue Windows 2000 o Windows XP, è necessario che sia installato almeno Windows 2000 SP3 o Windows XP SP1 per visualizzare la pagina **Imposta accesso al programma e impostazioni predefinite** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="f92d0-249">In Windows Vista e versioni successive, l'accesso alla pagina **Imposta accesso al programma e impostazioni predefinite computer** richiede privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="f92d0-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="f92d0-250">Per questo motivo, gli sviluppatori sono invitati a eseguire la registrazione per l'elemento [impostare i programmi predefiniti](default-programs.md) del pannello di controllo in modo che tutti gli utenti possano gestire le impostazioni predefinite dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="f92d0-251">Nell'albero del registro di sistema seguente viene illustrata la varietà di informazioni che devono essere registrate nella chiave **InstallInfo** del programma affinché il programma venga visualizzato nella pagina **Imposta accesso al programma e impostazioni predefinite computer** come opzione per il tipo di client.</span><span class="sxs-lookup"><span data-stu-id="f92d0-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="f92d0-252">Ognuno di questi valori viene descritto in dettaglio nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="f92d0-253">La riga di comando deve specificare un percorso assoluto completo del file, seguito da opzioni facoltative della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f92d0-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="f92d0-254">Utilizzare le virgolette appropriate per assicurarsi che gli spazi nella riga di comando non vengano interpretati erroneamente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="f92d0-255">Comando reinstalla</span><span class="sxs-lookup"><span data-stu-id="f92d0-255">The Reinstall Command</span></span>

<span data-ttu-id="f92d0-256">La riga di comando reinstalla dichiarata nel valore ReinstallCommand viene eseguita quando l'utente utilizza la pagina impostazione **impostazioni predefinite computer e accesso** al programma per selezionare il programma come predefinito per il tipo di client.</span><span class="sxs-lookup"><span data-stu-id="f92d0-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="f92d0-257">In Windows Vista e versioni successive, per accedere a questa pagina è necessario un livello di privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="f92d0-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="f92d0-258">In Windows 8, se l'applicazione è stata registrata con lo stesso nome sia per l'accesso al programma sia per le **impostazioni predefinite del computer** e per i **programmi predefiniti**, le impostazioni predefinite specificate nei **programmi predefiniti** per l'applicazione verranno applicate per l'utente corrente, nonché per l'esecuzione del comando reinstalla.</span><span class="sxs-lookup"><span data-stu-id="f92d0-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="f92d0-259">Il programma avviato dalla riga di comando REINSTALL deve associare l'applicazione al set completo dei tipi di [file](fa-intro.md) e di [protocollo](/previous-versions//aa767743(v=vs.85)) che l'applicazione è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="f92d0-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="f92d0-260">Tutte le applicazioni devono stabilire la funzionalità del gestore nel comando reinstalla.</span><span class="sxs-lookup"><span data-stu-id="f92d0-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="f92d0-261">Le applicazioni possono utilizzare il comando reinstalla per registrare la funzionalità e, facoltativamente, definire lo stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="f92d0-262">Quando un'applicazione sceglie di implementare sia la funzionalità che lo stato predefinito del gestore nel comando reinstalla, deve anche ripristinare eventuali collegamenti visibili o scelte rapide desiderate.</span><span class="sxs-lookup"><span data-stu-id="f92d0-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="f92d0-263">I punti di ingresso visibili scelti dalla maggior parte delle applicazioni sono elencati nel [comando Nascondi icone](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="f92d0-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-264">È consigliabile che le applicazioni implementino la funzionalità di gestione nel comando reinstalla.</span><span class="sxs-lookup"><span data-stu-id="f92d0-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="f92d0-265">Una volta completato il processo di reinstallazione, il programma avviato dalla riga di comando REINSTALL dovrebbe uscire.</span><span class="sxs-lookup"><span data-stu-id="f92d0-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="f92d0-266">Non deve avviare il programma corrispondente. deve semplicemente registrare i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="f92d0-267">Ad esempio, il comando reinstalla per un browser non deve aprire il home page dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-268">Per i client del browser e della posta elettronica in Windows XP e Windows Vista, le applicazioni che scelgono di stabilire la funzionalità di gestione e lo stato predefinito nel comando reinstalla devono registrarsi per l'icona corrispondente nella parte superiore del menu Start.</span><span class="sxs-lookup"><span data-stu-id="f92d0-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="f92d0-269">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione del menu Start](#start-menu-registration) .</span><span class="sxs-lookup"><span data-stu-id="f92d0-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="f92d0-270">Comando Nascondi icone</span><span class="sxs-lookup"><span data-stu-id="f92d0-270">The Hide Icons Command</span></span>

<span data-ttu-id="f92d0-271">La riga di comando dichiarata nel valore HideIconsCommand viene eseguita quando l'utente cancella la casella **Abilita accesso a questo programma** nella pagina **Imposta accesso al programma e impostazioni predefinite computer** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="f92d0-272">Questa riga di comando deve nascondere tutti i punti di accesso del programma visibili nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="f92d0-273">Le linee guida specifiche sono la rimozione di collegamenti e icone dalle posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f92d0-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="f92d0-274">Icone del desktop</span><span class="sxs-lookup"><span data-stu-id="f92d0-274">Desktop icons</span></span>
-   <span data-ttu-id="f92d0-275">Collegamenti al menu Start, incluso il gruppo di **avvio**</span><span class="sxs-lookup"><span data-stu-id="f92d0-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="f92d0-276">Collegamenti alla barra di avvio veloce</span><span class="sxs-lookup"><span data-stu-id="f92d0-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="f92d0-277">Area delle notifiche</span><span class="sxs-lookup"><span data-stu-id="f92d0-277">Notification area</span></span>
-   <span data-ttu-id="f92d0-278">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f92d0-278">Shortcut menus</span></span>
-   <span data-ttu-id="f92d0-279">Gruppo di attività cartella</span><span class="sxs-lookup"><span data-stu-id="f92d0-279">Folder task band</span></span>

<span data-ttu-id="f92d0-280">Questa riga di comando deve anche impedire chiamate automatiche del programma, ad esempio quelle specificate nella chiave **Run** del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f92d0-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="f92d0-281">I fornitori sono invitati a implementare queste linee guida nel callback Nascondi accesso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="f92d0-282">Non è necessario abbandonare la registrazione, ovvero la funzionalità dell'applicazione, dei tipi di file quando le icone sono nascoste.</span><span class="sxs-lookup"><span data-stu-id="f92d0-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="f92d0-283">Non è inoltre necessario abbandonare lo stato predefinito dell'applicazione per i tipi di file e di protocollo.</span><span class="sxs-lookup"><span data-stu-id="f92d0-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="f92d0-284">Questa operazione può causare un'esperienza utente errata quando questi tipi vengono rilevati nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="f92d0-285">Dopo aver nascosto le icone, è necessario aggiornare il valore del registro di sistema IconsVisible su 0, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f92d0-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="f92d0-286">La voce IconsVisible è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="f92d0-287">Metodo Hide Icon alternativo in SPAD</span><span class="sxs-lookup"><span data-stu-id="f92d0-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="f92d0-288">Per alcune applicazioni legacy, un'implementazione completa di Hide Access potrebbe non essere pratica.</span><span class="sxs-lookup"><span data-stu-id="f92d0-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="f92d0-289">Un metodo alternativo che ottiene lo stesso effetto è la disinstallazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="f92d0-290">La sezione seguente illustra il comportamento di esempio e il codice di esempio per implementare questa alternativa.</span><span class="sxs-lookup"><span data-stu-id="f92d0-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="f92d0-291">In generale, i fornitori di software indipendenti (ISV) devono evitare questa alternativa, perché sarà:</span><span class="sxs-lookup"><span data-stu-id="f92d0-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="f92d0-292">Disinstallare completamente l'applicazione dal sistema.</span><span class="sxs-lookup"><span data-stu-id="f92d0-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="f92d0-293">Rimuovere le impostazioni predefinite selezionate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f92d0-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="f92d0-294">Non lasciare alcuna opzione dell'interfaccia utente per reinstallare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="f92d0-295">Rendere la funzionalità Abilita accesso non più disponibile perché una disinstallazione rimuove completamente l'applicazione da SPAD.</span><span class="sxs-lookup"><span data-stu-id="f92d0-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="f92d0-296">L'esperienza utente consigliata è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f92d0-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="f92d0-297">Quando l'utente deseleziona la casella **Abilita l'accesso a questo programma** in SPAD, viene visualizzata l'interfaccia utente seguente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![finestra di dialogo per nascondere l'accesso al programma](images/hideaccessvista.png)

-   <span data-ttu-id="f92d0-299">Quando l'utente seleziona **OK**, viene avviato l'elemento **programmi e funzionalità** del pannello di controllo per consentire all'utente di disinstallare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="f92d0-300">Gli utenti di Windows XP devono essere visualizzati con questa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="f92d0-300">Windows XP users should be presented with this dialog box.</span></span>

    ![finestra di dialogo Windows XP equivalente](images/hideaccessxp.png)

-   <span data-ttu-id="f92d0-302">Quando l'utente di Windows XP seleziona **OK**, viene avviato l'elemento del pannello di controllo **Installazione applicazioni** per consentire all'utente di disinstallare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="f92d0-303">Il codice seguente fornisce un'implementazione riutilizzabile per la funzionalità Nascondi accesso, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f92d0-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="f92d0-304">Può essere utilizzato in Windows XP, Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f92d0-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="f92d0-305">Comando Mostra icone</span><span class="sxs-lookup"><span data-stu-id="f92d0-305">The Show Icons Command</span></span>

<span data-ttu-id="f92d0-306">La riga di comando dichiarata nella voce ShowIconsCommand viene eseguita quando l'utente seleziona la casella **Abilita l'accesso a questo programma** nella pagina **Imposta accesso al programma e impostazioni predefinite computer** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="f92d0-307">Questa riga di comando può ripristinare i punti di accesso del programma, inclusi quelli nel menu **Start** , sul desktop e nel gruppo di **avvio** , nonché le normali chiamate automatiche, ad esempio quelle specificate nella chiave **Run** del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f92d0-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="f92d0-308">I punti di accesso visibili di interesse per la maggior parte delle applicazioni sono elencati nel [comando Nascondi icone](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="f92d0-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="f92d0-309">L'applicazione non deve modificare le impostazioni predefinite per utente; tale modifica deve essere eseguita dall'utente tramite **programmi predefiniti**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="f92d0-310">Una volta visualizzate correttamente le icone, è necessario aggiornare il valore del registro di sistema IconsVisible a 1, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="f92d0-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="f92d0-311">Si noti che se è stata usata la voce HideIconsCommand per richiedere una disinstallazione dell'applicazione, la voce ShowIconsCommand non è usata.</span><span class="sxs-lookup"><span data-stu-id="f92d0-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="f92d0-312">Deve essere rimosso dal registro di sistema con le informazioni rimanenti dell'applicazione durante il processo di disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="f92d0-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="f92d0-313">Configurazione del programma di gruppo</span><span class="sxs-lookup"><span data-stu-id="f92d0-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-314">Questa sezione non si applica a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f92d0-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="f92d0-315">Come parte della preparazione del sistema, un OEM può stabilire una configurazione che nasconda i punti di accesso per il browser Microsoft, la posta elettronica, la riproduzione multimediale, la messaggistica istantanea o la macchina virtuale per i programmi client Java e specifica i propri programmi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="f92d0-316">Gli OEM possono consentire agli utenti di reimpostare i computer in qualsiasi momento a questa configurazione predefinita impostando i valori del registro di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="f92d0-317">Se queste chiavi sono impostate, gli utenti possono ripristinare la configurazione OEM selezionando l'opzione **produttore computer** nella pagina **Imposta accesso al programma e impostazioni predefinite computer** .</span><span class="sxs-lookup"><span data-stu-id="f92d0-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="f92d0-318">Se queste chiavi non sono impostate, l'opzione **produttore computer** non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="f92d0-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="f92d0-319">La voce **OEMShowIcons** , se presente, imposta lo stato di visualizzazione dell'icona per il client specificato che viene applicato se l'utente seleziona **produttore computer**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="f92d0-320">Il valore 1 indica che le icone vengono visualizzate e il valore 0 indica che le icone non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="f92d0-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="f92d0-321">Se **OEMShowIcons** è assente, la selezione del **produttore del computer** non ha alcun effetto sull'impostazione Mostra icona.</span><span class="sxs-lookup"><span data-stu-id="f92d0-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="f92d0-322">**OEMShowIcons** è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="f92d0-323">La voce **OEMDefault** , se presente e impostata su 1, stabilisce la preferenza OEM per il client predefinito del tipo indicato.</span><span class="sxs-lookup"><span data-stu-id="f92d0-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="f92d0-324">È possibile contrassegnare come predefinito OEM un solo client di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="f92d0-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="f92d0-325">Se più di una registrazione del client contiene la voce **OEMDefault** , verranno ignorate e il client corrente continuerà a essere usato come client predefinito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="f92d0-326">Se la voce **OEMDefault** non è presente o è impostata su 0, il client specifico non viene utilizzato come client predefinito se l'utente seleziona **produttore computer**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="f92d0-327">**OEMDefault** è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="f92d0-328">Oltre all'opzione per reimpostare i computer sulla configurazione predefinita stabilita dall'OEM, gli utenti dispongono di altre tre opzioni di configurazione:</span><span class="sxs-lookup"><span data-stu-id="f92d0-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="f92d0-329">Impostare il computer su una configurazione di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f92d0-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="f92d0-330">In questo caso, la pagina **set Program Access and computer defaults** consente l'accesso a tutti i software Microsoft e non Microsoft nel computer registrato nelle categorie di prodotti pertinenti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="f92d0-331">I programmi Microsoft Windows sono selezionati come opzione predefinita per ogni categoria.</span><span class="sxs-lookup"><span data-stu-id="f92d0-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="f92d0-332">Impostare il computer su una configurazione non Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f92d0-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="f92d0-333">Questa configurazione consente di nascondere i punti di accesso (ad esempio il menu **Start** ) a Windows Internet Explorer, Windows Media Player, Windows Messenger e Microsoft Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="f92d0-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="f92d0-334">Consente l'accesso al software non Microsoft nel computer in queste categorie.</span><span class="sxs-lookup"><span data-stu-id="f92d0-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="f92d0-335">Inoltre, se in una categoria è disponibile un programma non Microsoft, viene impostato come predefinito per tale categoria.</span><span class="sxs-lookup"><span data-stu-id="f92d0-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="f92d0-336">Se in una categoria è disponibile più di un programma non Microsoft, all'utente viene chiesto di scegliere il programma non Microsoft da usare come predefinito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="f92d0-337">Definire una configurazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f92d0-337">Establish a custom configuration.</span></span> <span data-ttu-id="f92d0-338">Gli utenti scelgono le proprie selezioni per abilitare o rimuovere l'accesso, combinando programmi Microsoft e non Microsoft nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="f92d0-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="f92d0-339">Gli utenti stabiliscono le opzioni predefinite in base alla categoria.</span><span class="sxs-lookup"><span data-stu-id="f92d0-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="f92d0-340">Gli utenti possono modificare una qualsiasi di queste opzioni in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="f92d0-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="f92d0-341">Esempio di registrazione del browser</span><span class="sxs-lookup"><span data-stu-id="f92d0-341">Browser Registration Example</span></span>

<span data-ttu-id="f92d0-342">Nell'esempio seguente viene illustrata la registrazione completa di **InstallInfo** per un browser di visualizzazione illuminato fittizio.</span><span class="sxs-lookup"><span data-stu-id="f92d0-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="f92d0-343">In questo caso, le opzioni della riga di comando consentono al file Litview.exe di eseguire qualsiasi azione necessaria per ogni valore.</span><span class="sxs-lookup"><span data-stu-id="f92d0-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="f92d0-344">Si noti che le virgolette vengono posizionate intorno ai percorsi perché contengono spazi incorporati.</span><span class="sxs-lookup"><span data-stu-id="f92d0-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="f92d0-345">Elementi di registrazione per tipi client specifici</span><span class="sxs-lookup"><span data-stu-id="f92d0-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="f92d0-346">Le informazioni seguenti sono reperibili anche nelle risorse elencate nella sezione Argomenti correlati alla fine di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f92d0-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="f92d0-347">Registrazione del menu Start</span><span class="sxs-lookup"><span data-stu-id="f92d0-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="f92d0-348">Registrazione client di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="f92d0-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="f92d0-349">Registrazione del menu Start</span><span class="sxs-lookup"><span data-stu-id="f92d0-349">Start Menu Registration</span></span>

<span data-ttu-id="f92d0-350">In Windows XP le applicazioni sono in genere registrate per impostazione predefinita in un ambito a livello di computer (**HKEY \_ locale \_**) anziché un utente (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="f92d0-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="f92d0-351">Con l'introduzione di Windows Vista del controllo dell'account utente, le applicazioni che attestano gli slot **Internet** e di **posta elettronica** nel menu **Start** devono implementare il comando reinstalla nel contesto di esecuzione corretto.</span><span class="sxs-lookup"><span data-stu-id="f92d0-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="f92d0-352">Il collegamento di **posta elettronica** del menu Start è stato rimosso a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f92d0-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="f92d0-353">Tuttavia, la registrazione descritta in questa sezione dovrebbe essere comunque eseguita perché assegna il client MAPI predefinito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="f92d0-354">Un utente con limitazioni su Windows XP, Windows Vista o Windows 7 non può accedere a SPAD.</span><span class="sxs-lookup"><span data-stu-id="f92d0-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="f92d0-355">Per questo motivo, gli sviluppatori sono invitati a eseguire la registrazione per l'elemento **impostare i programmi predefiniti** del pannello di controllo in modo che qualsiasi utente possa gestire le impostazioni predefinite dell'applicazione per utente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="f92d0-356">Le selezioni effettuate in SPAD devono avere effetto solo sulle impostazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="f92d0-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="f92d0-357">Impostare il valore del registro di sistema come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f92d0-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="f92d0-358">**Le informazioni seguenti si applicano solo a Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="f92d0-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="f92d0-359">Se la registrazione dell'impostazione predefinita a livello di computer nel computer \_ locale HKEY \_ come illustrato in precedenza ha esito positivo, l'applicazione deve eliminare il valore assegnato alla voce predefinita nella sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="f92d0-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="f92d0-360">Se la registrazione del valore predefinito a livello di computer nel computer \_ locale HKEY \_ come illustrato in precedenza ha esito negativo, in genere perché l'utente non dispone dell'autorizzazione di scrittura per la sottochiave, l'applicazione deve impostare il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="f92d0-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="f92d0-361">Il nome canonico viene registrato solo per l'utente corrente, non per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f92d0-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="f92d0-362">Dopo l'aggiornamento delle chiavi del registro di sistema, il programma deve trasmettere il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con **wParam** = 0 e **lParam** che punta alla stringa con terminazione null "software \\ clients \\ **ClientTypeName**" per notificare al sistema operativo che il client predefinito è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f92d0-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="f92d0-363">Registrazione client di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="f92d0-363">Mail Client Registration</span></span>

<span data-ttu-id="f92d0-364">Per un client di posta elettronica, è necessario che il programma disponga di impostazioni registrate sotto la chiave mailto **\_ \_ radice delle classi HKEY**, \\  in modo da soddisfare gli URL che utilizzano il `mailto` protocollo.</span><span class="sxs-lookup"><span data-stu-id="f92d0-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="f92d0-365">Impostare i valori e le chiavi che rispecchiano tali impostazioni nella chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="f92d0-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="f92d0-366">Questa gerarchia del registro di sistema sostituisce la `mailto` gerarchia esistente del registro di sistema disponibile in **HKEY \_ classi \_ radice** \\ **mailto**.</span><span class="sxs-lookup"><span data-stu-id="f92d0-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="f92d0-367">La gerarchia rimane invariata, ma solo il percorso è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f92d0-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="f92d0-368">Il formato di questa gerarchia è documentato in MSDN nelle panoramiche [e nelle esercitazioni del protocollo di collegamento asincrono](/previous-versions//aa767913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f92d0-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="f92d0-369">In genere, il `mailto` protocollo viene registrato in un programma anziché in un protocollo asincrono, nel qual caso viene applicata la documentazione relativa alla [registrazione di un'applicazione a uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f92d0-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="f92d0-370">Nell'esempio seguente viene illustrata la `mailto` sezione della registrazione per un `mailto` gestore registrato in un programma.</span><span class="sxs-lookup"><span data-stu-id="f92d0-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="f92d0-371">Il valore del registro di sistema flag è documentato in [tipi di file](fa-file-types.md) nella sezione intitolata "definizione degli attributi dei tipi di file".</span><span class="sxs-lookup"><span data-stu-id="f92d0-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="f92d0-372">Completa registrazioni di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-372">Complete Sample Registrations</span></span>

<span data-ttu-id="f92d0-373">Gli esempi seguenti sono forniti per mostrare i requisiti di registrazione completi per i vari tipi di client.</span><span class="sxs-lookup"><span data-stu-id="f92d0-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="f92d0-374">Un browser di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="f92d0-375">Un browser di posta elettronica di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="f92d0-376">Media Player di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="f92d0-377">Programma Instant Messenger di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="f92d0-378">Una macchina virtuale di esempio per Java</span><span class="sxs-lookup"><span data-stu-id="f92d0-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="f92d0-379">Un browser di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="f92d0-380">Un browser di posta elettronica di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="f92d0-381">Media Player di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="f92d0-382">Programma Instant Messenger di esempio</span><span class="sxs-lookup"><span data-stu-id="f92d0-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="f92d0-383">Una macchina virtuale di esempio per Java</span><span class="sxs-lookup"><span data-stu-id="f92d0-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="f92d0-384">*Le società, le organizzazioni, i prodotti, i nomi di dominio, gli indirizzi di posta elettronica, i logo, le persone, i luoghi e gli eventi di esempio descritti nel presente documento sono fittizi. Nessuna associazione con nessuna società, organizzazione, prodotto, nome di dominio, indirizzo di posta elettronica, logo, persona, luogo o evento è intenzionale o può essere presupposta.*</span><span class="sxs-lookup"><span data-stu-id="f92d0-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="f92d0-385">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f92d0-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f92d0-386">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="f92d0-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="f92d0-387">Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows</span><span class="sxs-lookup"><span data-stu-id="f92d0-387">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
</dt> <dt>

<span data-ttu-id="f92d0-388">[Layout del registro di sistema del client di Internet Explorer (vedere la sezione "definizioni della chiave del registro di sistema")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f92d0-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f92d0-389">[Panoramica ed esercitazioni sul protocollo di collegamento asincrono](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f92d0-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f92d0-390">[Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f92d0-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 
