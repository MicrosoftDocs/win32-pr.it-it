---
description: L'archiviazione di stringhe hardcoded nel registro di sistema fa parte di un modello di localizzazione precedente a Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Uso del reindirizzamento delle stringhe del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319472"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="96233-103">Uso del reindirizzamento delle stringhe del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="96233-103">Using Registry String Redirection</span></span>

<span data-ttu-id="96233-104">L'archiviazione di stringhe hardcoded nel registro di sistema fa parte di un modello di localizzazione precedente a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="96233-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="96233-105">Non è supportato da MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-105">It is not supported by MUI.</span></span> <span data-ttu-id="96233-106">Nel modello corrente, l'interfaccia utente per il sistema operativo viene eseguita in file di risorse specifici della lingua in base a una base indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="96233-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="96233-107">I componenti del sistema operativo utilizzano il registro di sistema in modo indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="96233-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="96233-108">MUI usa solo le stringhe del registro di sistema reindirizzate definite dalle risorse PE Win32 nel file di risorse della lingua di base.</span><span class="sxs-lookup"><span data-stu-id="96233-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="96233-109">Il reindirizzamento viene definito separatamente, ad esempio, in un file con estensione inf.</span><span class="sxs-lookup"><span data-stu-id="96233-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="96233-110">Questo tipo di archiviazione consente al caricatore di risorse di selezionare automaticamente le risorse di lingua corrette durante il caricamento del modulo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="96233-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="96233-111">Questo argomento riguarda solo le risorse PE di Win32.</span><span class="sxs-lookup"><span data-stu-id="96233-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="96233-112">Se si usano risorse PE non Win32, è necessario fornire il reindirizzamento personalizzato della stringa del registro di sistema, se necessario.</span><span class="sxs-lookup"><span data-stu-id="96233-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="96233-113">Creare una risorsa Language-Neutral</span><span class="sxs-lookup"><span data-stu-id="96233-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="96233-114">Un'applicazione MUI eseguita in Windows Vista e versioni successive utilizza una risorsa di stringa indipendente dal linguaggio per consentire l'accesso alle stringhe specifiche della lingua archiviate in una tabella delle risorse di stringa.</span><span class="sxs-lookup"><span data-stu-id="96233-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="96233-115">Il codice dell'applicazione che legge questi valori dal registro di sistema è descritto nella sezione caricare una Language-Neutral valore del registro di sistema di [individuazione delle stringhe reindirizzate](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="96233-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="96233-116">Il formato dei dati per un valore del registro di sistema indipendente dalla lingua è " `@<PE-path>,-<stringID>[;<comment>]` ", dove:</span><span class="sxs-lookup"><span data-stu-id="96233-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="96233-117">*PE-Path* specifica il percorso del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="96233-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="96233-118">Per supportare la distribuzione, è possibile specificare il percorso usando una variabile di ambiente, ad esempio% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="96233-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="96233-119">Un'alternativa alla creazione di un riferimento di stringa consiste nel lasciare le informazioni sul percorso del file.</span><span class="sxs-lookup"><span data-stu-id="96233-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="96233-120">In questo caso, l'applicazione deve avere un mezzo, ad esempio un altro valore del registro di sistema, per comunicare la propria directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="96233-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="96233-121">*stringID* specifica l'identificatore numerico della risorsa stringa pertinente, che viene implementato esattamente come qualsiasi altra risorsa di tipo stringa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="96233-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="96233-122">il *Commento* specifica informazioni facoltative per il debug o la leggibilità del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="96233-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="96233-123">Le funzioni API del registro di sistema ignorano il commento durante il caricamento della stringa.</span><span class="sxs-lookup"><span data-stu-id="96233-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="96233-124">I dati per il valore del registro di sistema non fanno riferimento esplicito al file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="96233-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="96233-125">Il file corretto viene determinato in fase di esecuzione, in base alle preferenze correnti della lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="96233-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="96233-126">Viene immesso un valore del registro di sistema senza uno spazio tra "," e "-".</span><span class="sxs-lookup"><span data-stu-id="96233-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="96233-127">Un valore del registro di sistema corretto è:</span><span class="sxs-lookup"><span data-stu-id="96233-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="96233-128">Il valore del registro di sistema non è corretto:</span><span class="sxs-lookup"><span data-stu-id="96233-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="96233-129">Un esempio di Windows Vista è il valore del registro di sistema con i dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="96233-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="96233-130">Creare risorse per le stringhe di collegamento</span><span class="sxs-lookup"><span data-stu-id="96233-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="96233-131">Quando l'applicazione MUI Visualizza il nome nell'interfaccia utente della shell, viene visualizzata una stringa InfoTip per l'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96233-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="96233-132">È necessario creare le risorse di stringa per il nome visualizzato dell'applicazione e la stringa InfoTip associata per ogni lingua supportata.</span><span class="sxs-lookup"><span data-stu-id="96233-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="96233-133">Quando le risorse sono pronte, l'applicazione può usare le stringhe come descritto in usare l'API shell per caricare le stringhe di collegamento dalla sezione del registro di sistema di [individuazione delle stringhe reindirizzate](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="96233-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="96233-134">Preparare le risorse per un collegamento creato con Windows Installer</span><span class="sxs-lookup"><span data-stu-id="96233-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="96233-135">Se si usa Windows Installer (MSI) per creare un collegamento, le risorse di stringa includono il nome visualizzato e la descrizione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="96233-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="96233-136">Nella [tabella dei collegamenti MSI](../msi/shortcut-table.md)viene fatto riferimento alla DLL delle risorse nelle colonne appropriate e gli identificatori di risorsa per il nome visualizzato e la descrizione del collegamento vengono usati nelle colonne dell'identificatore di risorsa corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="96233-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="96233-137">Affinché il collegamento dell'applicazione funzioni correttamente con la tecnologia delle risorse MUI, tenere presenti i seguenti punti quando si preparano le stringhe di collegamento:</span><span class="sxs-lookup"><span data-stu-id="96233-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="96233-138">Usare le variabili di ambiente o un percorso relativo per registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="96233-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="96233-139">È possibile specificare @% systemroot% \\ system32 \\shell32.dll purché il tipo di stringa del registro di sistema sia reg \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="96233-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="96233-140">L'identificatore di risorsa di stringa per "documento di testo" nel Shell32.dll è 12345.</span><span class="sxs-lookup"><span data-stu-id="96233-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="96233-141">Non usare spazi attorno ai simboli "," e "-".</span><span class="sxs-lookup"><span data-stu-id="96233-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="96233-142">Un esempio corretto è "shell32.dll,-22912".</span><span class="sxs-lookup"><span data-stu-id="96233-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="96233-143">Non usare un nome di file breve.</span><span class="sxs-lookup"><span data-stu-id="96233-143">Do not use a short file name.</span></span> <span data-ttu-id="96233-144">Questo tipo di nome non funziona con il caricatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="96233-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="96233-145">Preparare le risorse per un collegamento usando il formato INF</span><span class="sxs-lookup"><span data-stu-id="96233-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="96233-146">Se si usa il formato di file INF per creare stringhe di collegamento, il file di risorse deve apportare le impostazioni del registro di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="96233-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="96233-147">Queste istruzioni presuppongono l'uso della sintassi ProfileItems dell'API di installazione.</span><span class="sxs-lookup"><span data-stu-id="96233-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="96233-148">Modificare il valore InfoTip in modo che punti al riferimento di reindirizzamento di stringa, usando il percorso e l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="96233-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="96233-149">Aggiungere il nuovo valore DisplayResource nelle sezioni di installazione di ProfileItems.</span><span class="sxs-lookup"><span data-stu-id="96233-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="96233-150">Di seguito è riportato un esempio che illustra l'aggiunta dell'applicazione Calculator al menu **Start** :</span><span class="sxs-lookup"><span data-stu-id="96233-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="96233-151">Usare la sintassi illustrata di seguito quando si usa INF per aggiungere elementi, ad esempio una cartella del gruppo di accesso, al menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="96233-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="96233-152">Questa sintassi presuppone l'uso del \[ \] supporto StartMenuItems dal programma di installazione, simile alla sintassi utilizzata in Syssetup. inf.</span><span class="sxs-lookup"><span data-stu-id="96233-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="96233-153">Impostare il valore *infotip* sul riferimento di stringa " `@<path>,-resID` ".</span><span class="sxs-lookup"><span data-stu-id="96233-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="96233-154">Il nome visualizzato è determinato dai valori *resDLL* e *da un Resid* .</span><span class="sxs-lookup"><span data-stu-id="96233-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="96233-155">Il valore *da un Resid* specifica l'identificatore di risorsa per una risorsa di stringa associata al file indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="96233-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="96233-156">Il valore *resDLL* specifica il percorso del file indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="96233-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="96233-157">Creare risorse per i nomi descrittivi dei tipi di documento</span><span class="sxs-lookup"><span data-stu-id="96233-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="96233-158">È necessario implementare le stringhe nome descrittivo e InfoTip per l'applicazione come risorse di stringa.</span><span class="sxs-lookup"><span data-stu-id="96233-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="96233-159">Per consentire i nomi dei tipi di documenti descrittivi per rispondere alla lingua dell'interfaccia utente, l'applicazione deve registrare i nomi usando il valore FriendlyTypeName sotto la chiave identificatore del programma per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="96233-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="96233-160">Per mantenere la compatibilità con le versioni precedenti, è necessario conservare il valore predefinito per la chiave dell'identificatore del programma.</span><span class="sxs-lookup"><span data-stu-id="96233-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="96233-161">Per informazioni sull'accesso ai nomi dall'applicazione, vedere i nomi dei tipi di documento descrittivo per la query nella sezione del registro di sistema per [individuare le stringhe reindirizzate](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="96233-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="96233-162">Il lavoro specifico prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="96233-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="96233-163">Implementare il nome descrittivo e le stringhe InfoTip come risorse di stringa specifiche della lingua.</span><span class="sxs-lookup"><span data-stu-id="96233-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="96233-164">Aggiungere il valore FriendlyTypeName sotto la chiave del registro di sistema del tipo di documento.</span><span class="sxs-lookup"><span data-stu-id="96233-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="96233-165">I dati per il valore seguono il modello " `@<path>,-<resID>` ", dove *path* indica il file eseguibile e *da un Resid* è l'identificatore di risorsa di una risorsa di tipo stringa localizzabile associata a tale eseguibile.</span><span class="sxs-lookup"><span data-stu-id="96233-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="96233-166">Specificare il valore del registro di sistema InfoTip in base al formato " `@<path>,-<resID>` ".</span><span class="sxs-lookup"><span data-stu-id="96233-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="96233-167">Nell'esempio seguente vengono illustrate le impostazioni del registro di sistema per un file con estensione txt:</span><span class="sxs-lookup"><span data-stu-id="96233-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="96233-168">Fornire risorse per le stringhe di azione dei verbi della shell</span><span class="sxs-lookup"><span data-stu-id="96233-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="96233-169">Le stringhe di azione per determinati verbi, ad esempio "Open" e "Edit", vengono visualizzate nel menu a comparsa visualizzato quando l'utente fa clic con il pulsante destro del mouse su un file in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="96233-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="96233-170">Non è necessario che l'applicazione specifichi stringhe per i verbi comuni della shell, perché per questi verbi la shell ha le proprie impostazioni predefinite abilitate per MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="96233-171">Tuttavia, è necessario fornire risorse di stringa localizzabili per le stringhe che rappresentano i verbi non comuni.</span><span class="sxs-lookup"><span data-stu-id="96233-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="96233-172">Nei sistemi operativi precedenti a Windows XP, viene eseguito il rendering delle stringhe per i verbi della shell nel registro di sistema utilizzando la sintassi seguente, dove *verbo* specifica il nome effettivo del verbo:</span><span class="sxs-lookup"><span data-stu-id="96233-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="96233-173">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="96233-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="96233-174">In Windows XP e versioni successive, è possibile utilizzare un livello di riferimento indiretto per fare in modo che una stringa di azione dipenda dalla lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="96233-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="96233-175">Questi sistemi operativi supportano un valore MUIVerb per la definizione di una stringa compatibile con MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="96233-176">Di seguito è riportato un esempio di una voce del registro di sistema per un verbo non comune:</span><span class="sxs-lookup"><span data-stu-id="96233-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="96233-177">L'applicazione MUI dovrebbe inoltre essere in grado di registrare il valore predefinito precedente come stringa localizzabile, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="96233-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="96233-178">La registrazione del valore predefinito precedente non è consigliata perché richiede una configurazione diversa in Windows XP e versioni successive rispetto alla configurazione usata nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="96233-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="96233-179">Creazione di risorse per verbi, protocolli e stringhe AuxUserType</span><span class="sxs-lookup"><span data-stu-id="96233-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="96233-180">È necessario creare risorse di stringa localizzabili per le stringhe verb, Protocol e AuxUserType.</span><span class="sxs-lookup"><span data-stu-id="96233-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="96233-181">Usare le impostazioni del registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="96233-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="96233-182">Il valore specificato per LocalizedString contiene o sostituisce solo il valore per il *verbo*, non i due valori di flag.</span><span class="sxs-lookup"><span data-stu-id="96233-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="96233-183">Di seguito è riportato un riepilogo per garantire la correttezza delle impostazioni del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="96233-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="96233-184">Se CLSID contiene una \\ \\ chiave inseribile CLSID {CLSID} HKCR \\ , definire il valore CLSID predefinito utilizzando HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="96233-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="96233-185">Se CLSID contiene una o più sottochiavi sotto il \\ verbo HKCR CLSID \\ {CLSID} \\ , definire ogni singola stringa del verbo usando HKCR \\ CLSID \\ {CLSID} \\ Verb \\ xxx \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="96233-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="96233-186">Se CLSID ha una o più sottochiavi sotto il \\ verbo StdFileEditing del protocollo HKCR {ProgID} \\ \\ \\ , definire ogni singola stringa del verbo usando il \\ verbo StdFileEditing di HKCR {ProgID} \\ protocollo \\ \\ \\ xxx \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="96233-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="96233-187">Se CLSID contiene una o più sottochiavi AuxUserType elencate in HKCR \\ CLSID \\ {CLSID} \\ AuxUserType, definire ogni voce AuxUserType usando HKCR \\ CLSID \\ {CLSID} \\ AuxUserType \\ xxx LocalizedString \\ .</span><span class="sxs-lookup"><span data-stu-id="96233-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="96233-188">Creare una risorsa per il programma di disinstallazione</span><span class="sxs-lookup"><span data-stu-id="96233-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="96233-189">Per registrare il programma di disinstallazione per l'applicazione, è possibile creare i valori del registro di sistema nella sottochiave identificatore univoco per l'applicazione nella chiave del registro di sistema HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall.</span><span class="sxs-lookup"><span data-stu-id="96233-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="96233-190">I valori da impostare includono: DisplayName, DisplayVersion, Publisher, ProductID, regownr, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, comments, DisplayIcon, Readme, UrlUpdateInfo.</span><span class="sxs-lookup"><span data-stu-id="96233-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="96233-191">Per abilitare la tecnologia MUI per ogni valore, è possibile aggiungere " \_ localizzato" al nome del valore.</span><span class="sxs-lookup"><span data-stu-id="96233-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="96233-192">I componenti del sistema operativo sono necessari per fornire un valore per DisplayName \_ localizzato in modo specifico per MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="96233-193">È necessario inserire il nome visualizzato in una DLL, ad esempio Res.dll, come una risorsa di tipo stringa, supponendo che l'identificatore sia 1245.</span><span class="sxs-lookup"><span data-stu-id="96233-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="96233-194">L'applicazione può quindi registrare il nome visualizzato come DisplayName \_ localizzato con il valore "@ \\res.DLL,-1245".</span><span class="sxs-lookup"><span data-stu-id="96233-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="96233-195">Tutte le altre impostazioni del registro di sistema devono essere mantenute così come sono, incluso il valore originale per DisplayName.</span><span class="sxs-lookup"><span data-stu-id="96233-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="96233-196">Creazione di risorse per eventi audio</span><span class="sxs-lookup"><span data-stu-id="96233-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="96233-197">Windows associa determinati eventi a file audio, ad esempio un nuovo evento di notifica di posta elettronica o un evento di allarme batteria critico.</span><span class="sxs-lookup"><span data-stu-id="96233-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="96233-198">I nomi degli eventi devono essere visualizzati dall'interfaccia utente e devono supportare la globalizzazione.</span><span class="sxs-lookup"><span data-stu-id="96233-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="96233-199">Pertanto, è necessario implementare una risorsa di stringa localizzabile per la descrizione di ogni descrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="96233-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="96233-200">Aggiungere un nuovo valore del registro di sistema per ogni nome di evento, oltre al valore predefinito hardcoded.</span><span class="sxs-lookup"><span data-stu-id="96233-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="96233-201">Per abilitare un evento audio, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="96233-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="96233-202">Implementare la descrizione come una risorsa di stringa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="96233-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="96233-203">Aggiungere un nuovo valore del registro di sistema per il nome visualizzato, oltre al valore predefinito hardcoded.</span><span class="sxs-lookup"><span data-stu-id="96233-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="96233-204">Il layout del registro di sistema associato è illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="96233-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="96233-205">Se la shell non riesce a trovare o recuperare il valore di DispFileName, viene usata la descrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="96233-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="96233-206">Creare risorse per le stringhe di layout della tastiera</span><span class="sxs-lookup"><span data-stu-id="96233-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="96233-207">Se l'applicazione implementa un layout di tastiera, richiede una risorsa di stringa localizzabile per il nome del layout per la visualizzazione dello schermo, ad esempio negli elenchi dei layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="96233-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="96233-208">Ogni layout di tastiera ha una chiave del registro di sistema in HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ keyboard layouts.</span><span class="sxs-lookup"><span data-stu-id="96233-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="96233-209">Tra i valori per tale chiave si trovano testo di layout, un nome leggibile per la compatibilità con le versioni precedenti e il nome visualizzato del layout.</span><span class="sxs-lookup"><span data-stu-id="96233-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="96233-210">I dati forniti per il nome visualizzato del layout devono essere un riferimento di stringa nel formato " `@<path>,-resID` ", che fa riferimento a una risorsa di tipo stringa localizzabile associata al layout della tastiera.</span><span class="sxs-lookup"><span data-stu-id="96233-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="96233-211">Di seguito è riportato un esempio di impostazione del registro di sistema per il layout di tastiera spagnolo (Spagna):</span><span class="sxs-lookup"><span data-stu-id="96233-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="96233-212">Rappresenta stringhe della finestra di dialogo comuni dell'oggetto Insert OLE</span><span class="sxs-lookup"><span data-stu-id="96233-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="96233-213">È possibile implementare il nome visualizzato di un oggetto OLE Insertable come risorsa di stringa localizzabile associata al codice che implementa tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="96233-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="96233-214">La finestra di [dialogo OLE Inserisci oggetto](/cpp/mfc/reference/coleinsertdialog-class) ottiene un nome visualizzato dalla chiave del registro \\ di sistema HKCR CLSID \\ { *<GUID>* }, dove *GUID* identifica l'identificatore di classe di un oggetto OLE inseribile.</span><span class="sxs-lookup"><span data-stu-id="96233-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="96233-215">Windows Vista e versioni successive implementano questo tipo di oggetto in modo localizzabile, usando un nome visualizzato compatibile con MUI che consente la personalizzazione della lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="96233-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="96233-216">Al contrario, i sistemi operativi precedenti a Windows Vista implementano il nome visualizzato per questo tipo di oggetto utilizzando il valore predefinito della chiave del registro di sistema corrispondente.</span><span class="sxs-lookup"><span data-stu-id="96233-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="96233-217">Questo nome è in genere un nome in lingua inglese (Stati Uniti) o un nome nella lingua dell'interfaccia utente predefinita del sistema.</span><span class="sxs-lookup"><span data-stu-id="96233-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="96233-218">Non tutti gli oggetti che corrispondono alle sottochiavi della chiave del registro di sistema sono inseribili.</span><span class="sxs-lookup"><span data-stu-id="96233-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="96233-219">Il valore predefinito della \\ \\ chiave CLSID { *<GUID>* } HKCR deve conservare un nome leggibile per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="96233-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="96233-220">Tuttavia, deve definire anche il valore LocalizedString, nel formato " `@<path>,-ResID` ", dove path identifica il file eseguibile che implementa l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="96233-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="96233-221">Il valore da un Resid specifica l'identificatore di risorsa della stringa localizzabile per il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="96233-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="96233-222">Ad esempio, lo script di registrazione per l'oggetto Insertable media clip include le righe seguenti:</span><span class="sxs-lookup"><span data-stu-id="96233-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="96233-223">La prima riga fornisce la compatibilità con le versioni precedenti inserendo una stringa di testo semplice nel registro di sistema come nome visualizzato predefinito.</span><span class="sxs-lookup"><span data-stu-id="96233-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="96233-224">La seconda riga consente di accedere al nome visualizzato compatibile con MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="96233-225">Indica l'identificatore di stringa archiviato in Mplay32.exe.</span><span class="sxs-lookup"><span data-stu-id="96233-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="96233-226">La stringa con identificatore 9217 in Mplay32.exe può essere associata a valori di risorse stringa per un numero qualsiasi di lingue.</span><span class="sxs-lookup"><span data-stu-id="96233-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="96233-227">Il nome inglese (Stati Uniti) è "clip multimediale".</span><span class="sxs-lookup"><span data-stu-id="96233-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="96233-228">Creare risorse di stringa per Microsoft Management Console Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="96233-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="96233-229">È necessario creare una risorsa di stringa localizzabile per ogni snap-in di Microsoft Management Console (MMC) usato dall'applicazione MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="96233-230">Poiché lo snap-in fa parte di una console di, dispone di un'interfaccia utente e deve essere globalizzato per operare in più linguaggi.</span><span class="sxs-lookup"><span data-stu-id="96233-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="96233-231">Nella maggior parte dei casi, gli snap-in MMC generano gli stessi problemi di globalizzazione e localizzazione dell'applicazione MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="96233-232">Uno snap-in di MMC deve riflettere il nome nel registro di sistema per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="96233-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="96233-233">La voce del registro di sistema deve includere sia un riferimento indiretto a una risorsa stringa localizzabile che una stringa letterale per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="96233-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="96233-234">Ogni snap-in MMC dispone di una chiave del registro di sistema in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ MMC \\ snap-in.</span><span class="sxs-lookup"><span data-stu-id="96233-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="96233-235">Tra i valori per la chiave sono NameString, specificando un nome leggibile per la compatibilità con le versioni precedenti e NameStringIndirect, specificando un riferimento indiretto a una risorsa di stringa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="96233-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="96233-236">Per NameStringIndirect, è necessario fornire un riferimento di stringa nel formato " `@<path>,-resID` ", che rappresenta una risorsa stringa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="96233-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="96233-237">Ad esempio, è possibile impostare l'impostazione seguente per Mymmc.dll, dove 12345 è l'identificatore della risorsa stringa corrispondente contenente il nome localizzabile dello snap-in:</span><span class="sxs-lookup"><span data-stu-id="96233-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="96233-238">Alcuni snap-in registrano altri valori stringa del registro di sistema che MMC non legge dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="96233-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="96233-239">Per ulteriori informazioni sull'utilizzo di questi valori, vedere registrare Microsoft Management Console Snap-In stringhe non lette dal registro di sistema in [individuazione di stringhe reindirizzate](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="96233-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="96233-240">Creare risorse di stringa per un servizio Windows</span><span class="sxs-lookup"><span data-stu-id="96233-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="96233-241">Sebbene un servizio di Windows in genere disponga di un'interfaccia utente piccola o nessuna, deve visualizzare un nome conforme a MUI e in genere fornisce una descrizione specifica del linguaggio compatibile con MUI.</span><span class="sxs-lookup"><span data-stu-id="96233-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="96233-242">La chiave del registro di sistema che descrive un servizio Windows supporta solo il valore DisplayName per il nome del servizio e il valore Description per la descrizione del servizio.</span><span class="sxs-lookup"><span data-stu-id="96233-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="96233-243">Le impostazioni per il servizio Windows vengono effettuate dall'applicazione, come descritto in impostare il nome visualizzato e la descrizione di un servizio Windows dal registro di sistema in [individuazione delle stringhe reindirizzate](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="96233-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="96233-244">Se l'applicazione non imposta i valori del registro di sistema per l'interfaccia utente del servizio, i valori nel registro di sistema rimangono impostati sull'inglese, anche se l'interfaccia utente è in un'altra lingua.</span><span class="sxs-lookup"><span data-stu-id="96233-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96233-245">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96233-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96233-246">Preparazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="96233-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="96233-247">Individuazione di stringhe reindirizzate</span><span class="sxs-lookup"><span data-stu-id="96233-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 
