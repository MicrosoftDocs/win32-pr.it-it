---
description: Il compilatore Managed Object Format (MOF) analizza un file contenente istruzioni MOF e aggiunge le classi e le istanze di classe definite nel file al repository WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879969"
---
# <a name="mofcomp"></a><span data-ttu-id="a2b5a-103">mofcomp</span><span class="sxs-lookup"><span data-stu-id="a2b5a-103">mofcomp</span></span>

<span data-ttu-id="a2b5a-104">Il compilatore [*Managed Object Format (MOF)*](gloss-m.md) analizza un file contenente istruzioni MOF e aggiunge le classi e le istanze di classe definite nel file al repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="a2b5a-105">I file MOF vengono in genere compilati automaticamente durante l'installazione dei sistemi con cui vengono forniti, ma è anche possibile compilare file MOF utilizzando questo strumento.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="a2b5a-106">Per ulteriori informazioni sull'individuazione e sull'utilizzo di mofcomp.exe, vedere [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="a2b5a-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="a2b5a-107">Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando per il preprocessore [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="a2b5a-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="a2b5a-108">Nell'esempio di codice seguente viene illustrato come eseguire il compilatore MOF in un file.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="a2b5a-109">Commutatori</span><span class="sxs-lookup"><span data-stu-id="a2b5a-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="a2b5a-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-recupero automatico**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-111">Aggiunge il file MOF denominato all'elenco di file compilati durante il ripristino del repository.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="a2b5a-112">L'elenco dei file MOF di recupero automatico è archiviato nella chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="a2b5a-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="a2b5a-113">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="a2b5a-114">I file MOF elencati in questa voce del registro di sistema devono trovarsi nel computer locale perché i file MOF che usano il comando **autocover** non possono ripristinare i file MOF presenti in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="a2b5a-115">Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file [*Managed Object Format*](gloss-m.md) (MOF).</span><span class="sxs-lookup"><span data-stu-id="a2b5a-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="a2b5a-116"><span id="-check"></span><span id="-CHECK"></span>**-controllo**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-117">Richiede che il compilatore esegua solo una verifica della sintassi e visualizzi i messaggi di errore appropriati.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="a2b5a-118">Non è possibile usare altre opzioni con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="a2b5a-119">Quando si utilizza questa opzione, non viene stabilita alcuna connessione a Strumentazione gestione Windows (WMI) e non vengono apportate modifiche al repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _namespacePath_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="a2b5a-121">Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacePath*.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="a2b5a-122">Il file MOF compilato viene caricato nello spazio dei nomi mofcomp predefinito, \\ valore predefinito radice, a meno che non venga usata questa opzione.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="a2b5a-123">È anche possibile inserire lo **\# spazio dei nomi pragma** del comando per il preprocessore ("_percorso dello spazio dei nomi_*_")_* nel file MOF per ottenere lo stesso effetto.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="a2b5a-124">Se vengono usati sia l'opzione **-N:** che il \# comando <a href="pragma-namespace.md">pragma namespace</a> , il \# **pragma namespace** **autocover** ha la priorità.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="a2b5a-125">In questo caso, l'unico modo per compilare il file MOF in un altro spazio dei nomi consiste nel modificare il file MOF e modificare il \# comando **pragma namespace** .</span><span class="sxs-lookup"><span data-stu-id="a2b5a-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="a2b5a-126">È possibile specificare un computer remoto utilizzando \\ \\ MachineName \\ root \\ default.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="a2b5a-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Classe: createonly**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-128">Richiede che il compilatore non modifichi le classi esistenti.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="a2b5a-129">Quando si utilizza questa opzione, l'operazione di compilazione termina se esiste già una classe specificata nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Classe: ForceUpdate**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-131">Forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="a2b5a-132">Si supponga, ad esempio, che un qualificatore di classe venga definito in una classe figlio e che la classe base tenti di aggiungere lo stesso qualificatore.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="a2b5a-133">In **-Class: ForceUpdate** Mode, il compilatore MOF risolve il conflitto eliminando il qualificatore in conflitto nella classe figlio.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="a2b5a-134">Se la classe figlio dispone di istanze, l'aggiornamento forzato avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Classe: safeupdate**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-136">Consente di aggiornare le classi anche se sono presenti classi figlio, purché la modifica non causi conflitti con le classi figlio.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="a2b5a-137">Questo flag, ad esempio, consente di aggiungere una nuova proprietà alla classe di base non citata in precedenza nelle classi figlio.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="a2b5a-138">Se le classi figlio hanno istanze, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Classe: updateonly**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-140">Richiede che il compilatore non crei nuove classi.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="a2b5a-141">Quando si utilizza questa opzione, l'operazione di compilazione termina se non esiste una classe specificata nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-istanza: updateonly**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-143">Richiede che il compilatore non crei nuove istanze.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="a2b5a-144">Quando si utilizza questa opzione, l'operazione di compilazione termina se non esiste un'istanza specificata nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-istanza: createonly**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-146">Richiede che il compilatore non modifichi le istanze esistenti.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="a2b5a-147">Quando si utilizza questa opzione, l'operazione di compilazione termina se un'istanza specificata nel file MOF esiste già.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _filename_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-149">Richiede che il compilatore crei una versione binaria del file MOF con il nome *filename* senza apportare alcuna modifica al repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="a2b5a-150">Se si usa l'opzione **-B: <** _filename_ *_>_* per creare un file MOF binario, solo le versioni dei qualificatori predefinite vengono archiviate nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="a2b5a-151">Il formato MOF binario è il formato intermedio per combinare un driver WDM con il file MOF come risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="a2b5a-152">Il MOF binario rappresenta le classi e le istanze come un file MOF di testo e viene compresso prima di essere archiviato su disco.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-154">Richiede che il compilatore esegua un controllo della sintassi WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="a2b5a-155">Con questa opzione è necessario usare l'opzione **-B:** .</span><span class="sxs-lookup"><span data-stu-id="a2b5a-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="a2b5a-156">L'opzione **-WMI** viene utilizzata solo per la compilazione di file MOF binari per l'utilizzo da parte dei driver di dispositivo WDM.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="a2b5a-157">Questa opzione richiama un controllo file MOF binario separato, che viene eseguito dopo la creazione del file MOF binario.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _password_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-159">Specifica *la password per* l'utente del computer da immettere al momento dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:** _nome utente_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-161">Specifica *username* come nome dell'utente che ha effettuato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: <** _autorità_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-163">Specifica l' *autorità* come autorità (nome di dominio) da usare per l'accesso a WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:** _percorso_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-165">Nome dell'output indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-165">Name of the language neutral output.</span></span> <span data-ttu-id="a2b5a-166">Utilizzato con l'opzione **-emendamento** per specificare il nome del file MOF indipendente dalla lingua che verrà generato.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:** _percorso_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-168">Nome dell'output specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-168">Name of the language specific output.</span></span> <span data-ttu-id="a2b5a-169">Utilizzato con l'opzione **-emendamento** per specificare il nome del file MOF specifico della lingua che verrà generato.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Modifica:** _impostazioni locali_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-171">Suddivide il file MOF in versioni specifiche della lingua e indipendenti dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="a2b5a-172">Il compilatore MOF crea una forma indipendente dal linguaggio del file MOF con tutti i qualificatori modificati rimossi.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="a2b5a-173">Viene creata anche una versione localizzata del file MOF con un'estensione di file MFL.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="a2b5a-174">Il parametro *locale* specifica il nome dello spazio dei nomi figlio che contiene le definizioni di classe localizzate.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="a2b5a-175">Il formato del parametro delle *impostazioni locali* è MS \_ xxx, dove xxx è il valore esadecimale dell'LCID di Windows.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="a2b5a-176">Ad esempio, le impostazioni locali per l'inglese americano sono MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-178">Estrae MOF binario da una risorsa denominata.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="a2b5a-179">Questa opzione ottiene il file MOF binario dalla classe nel repository WMI mentre l'opzione-B crea il formato MOF binario da un file MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ResourceLocale_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-181">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-181">Optional.</span></span> <span data-ttu-id="a2b5a-182">Estrae le descrizioni MOF localizzate dal MOF binario quando viene usato con l'opzione-ER.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a2b5a-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-184">Nome del file da analizzare.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="a2b5a-185">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="a2b5a-185">Return Values</span></span>

<span data-ttu-id="a2b5a-186">Come prima operazione, il compilatore MOF esegue un controllo della sintassi sul file MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="a2b5a-187">Se il compilatore rileva errori, viene stampato un messaggio di errore e il processo viene terminato.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="a2b5a-188">Il compilatore MOF può restituire i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2b5a-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="a2b5a-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="a2b5a-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-190">Operazione di compilazione MOF completata.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="a2b5a-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-192">Il compilatore MOF non è riuscito a connettersi al server WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="a2b5a-193">Questo problema si verifica a causa di un errore semantico, ad esempio un'incompatibilità con il repository WMI esistente, oppure un errore effettivo, ad esempio l'avvio del server WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="a2b5a-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-195">Una o più opzioni della riga di comando non sono valide.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a2b5a-196"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="a2b5a-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="a2b5a-197">Si è verificato un errore di sintassi MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="a2b5a-198">Se il file MOF viene analizzato correttamente, ma viene effettuato un tentativo di eseguire un'operazione non consentita da un'opzione della riga di comando, il compilatore restituisce un codice di errore generato da WMI anziché uno dei codici restituiti elencati nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="a2b5a-199">Ad esempio, viene restituito un codice di errore WMI quando viene specificata l'opzione **-instance: updateonly** e il file MOF tenta di creare un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="a2b5a-200">Se l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) non è presente nel file, viene restituito l'avviso seguente:</span><span class="sxs-lookup"><span data-stu-id="a2b5a-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="a2b5a-201">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2b5a-201">Remarks</span></span>

<span data-ttu-id="a2b5a-202">Il compilatore MOF è disponibile nella directory% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="a2b5a-203">È necessario specificare il file MOF come parametro del compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="a2b5a-204">È anche possibile specificare un'opzione di recupero automatico se si vuole che il file MOF venga ricompilato automaticamente se il repository CIM deve essere recuperato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="a2b5a-205">Per ulteriori informazioni, digitare **mofcomp/?**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="a2b5a-206">al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-206">at the command prompt.</span></span>

<span data-ttu-id="a2b5a-207">Un file MOF che utilizza il set di caratteri Unicode contiene una firma come i primi due byte del file.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="a2b5a-208">Questa firma è U + FFFE o U + FEFF, a seconda dell'ordine dei byte del file.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="a2b5a-209">Quando non si verificano errori nel processo di analisi, il compilatore MOF si connette al server WMI in esecuzione nel computer locale, a meno che non sia stata specificata l'opzione **-Check** .</span><span class="sxs-lookup"><span data-stu-id="a2b5a-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="a2b5a-210">Le classi e le istanze definite nel file MOF vengono aggiunte al repository WMI.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="a2b5a-211">Quando si verifica un errore durante l'aggiornamento del repository WMI, il compilatore non esegue alcun tentativo di riportare il repository allo stato precedente all'inizio dell'elaborazione del compilatore.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="a2b5a-212">**Windows 8:** Quando si installa un provider, mofcomp considera la \[ chiave \] e i \[ \] qualificatori statici come true se sono presenti, indipendentemente dai valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="a2b5a-213">Altri qualificatori vengono considerati false se sono presenti ma non sono impostati in modo esplicito su true.</span><span class="sxs-lookup"><span data-stu-id="a2b5a-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b5a-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2b5a-214">Requirements</span></span>



| <span data-ttu-id="a2b5a-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2b5a-215">Requirement</span></span> | <span data-ttu-id="a2b5a-216">Valore</span><span class="sxs-lookup"><span data-stu-id="a2b5a-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a2b5a-217">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2b5a-217">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b5a-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2b5a-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a2b5a-219">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2b5a-219">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b5a-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2b5a-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2b5a-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2b5a-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b5a-222">**spazio dei nomi pragma**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="a2b5a-223">Compilazione di file MOF</span><span class="sxs-lookup"><span data-stu-id="a2b5a-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="a2b5a-224">Compilazione di file MOF localizzati</span><span class="sxs-lookup"><span data-stu-id="a2b5a-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="a2b5a-225">Registrazione di un provider</span><span class="sxs-lookup"><span data-stu-id="a2b5a-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="a2b5a-226">**IMOFCompiler:: CompileFile**</span><span class="sxs-lookup"><span data-stu-id="a2b5a-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

