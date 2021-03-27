---
description: Per gli elementi del pannello di controllo implementati come file con estensione exe, non è necessaria alcuna esportazione o gestione dei messaggi speciale. Qualsiasi file con estensione exe può essere registrato come oggetto Command per essere visualizzato con un punto di ingresso nella cartella del pannello di controllo.
title: Come registrare gli elementi del pannello di controllo eseguibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050000"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="21fd1-104">Come registrare gli elementi del pannello di controllo eseguibile</span><span class="sxs-lookup"><span data-stu-id="21fd1-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="21fd1-105">Per gli elementi del pannello di controllo implementati come file con estensione exe, non è necessaria alcuna esportazione o gestione dei messaggi speciale.</span><span class="sxs-lookup"><span data-stu-id="21fd1-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="21fd1-106">Qualsiasi file con estensione exe può essere registrato come oggetto Command per essere visualizzato con un punto di ingresso nella cartella del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="21fd1-107">Un esempio viene usato qui per illustrare i requisiti di registrazione.</span><span class="sxs-lookup"><span data-stu-id="21fd1-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="21fd1-108">Nell'esempio viene illustrato come registrare un elemento del pannello di controllo denominato **impostazioni personali** come oggetto comando, in modo che venga visualizzato nella finestra del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="21fd1-109">La finestra **impostazioni personali** viene visualizzata anche quando `MyApp.exe /settings` viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="21fd1-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="21fd1-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="21fd1-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="21fd1-111">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="21fd1-111">Step 1:</span></span>

<span data-ttu-id="21fd1-112">Genera un GUID per l'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="21fd1-113">Il GUID identifica in modo univoco l'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="21fd1-114">In questo esempio, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` è il GUID dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="21fd1-115">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="21fd1-115">Step 2:</span></span>

<span data-ttu-id="21fd1-116">Utilizzando il GUID come nome, aggiungere una sottochiave al registro di sistema come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="21fd1-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="21fd1-117">I dati per la voce predefinita sono semplicemente il \_ nome di reg SZ dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="21fd1-118">La voce predefinita può essere utile per identificare la voce del GUID, ma è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="21fd1-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="21fd1-119">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="21fd1-119">Step 3:</span></span>

<span data-ttu-id="21fd1-120">Utilizzando il GUID come nome, aggiungere una sottochiave e le relative voci al registro di sistema come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="21fd1-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="21fd1-121">**Default**.</span><span class="sxs-lookup"><span data-stu-id="21fd1-121">**Default**.</span></span> <span data-ttu-id="21fd1-122">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="21fd1-122">REG\_SZ.</span></span> <span data-ttu-id="21fd1-123">Nome visualizzato per l'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="21fd1-124">**LocalizedString**.</span><span class="sxs-lookup"><span data-stu-id="21fd1-124">**LocalizedString**.</span></span> <span data-ttu-id="21fd1-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-125">Optional.</span></span> <span data-ttu-id="21fd1-126">REG \_ sz o reg \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="21fd1-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="21fd1-127">Il nome del modulo e l'ID della tabella di stringhe del nome localizzato dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="21fd1-128">Il formato è un segno di chiocciola (@) seguito dal nome del file con estensione exe o dll che contiene la tabella delle stringhe MUI (Multilingual User Interface).</span><span class="sxs-lookup"><span data-stu-id="21fd1-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="21fd1-129">Le variabili di ambiente possono essere usate come sostituzioni per una parte del percorso.</span><span class="sxs-lookup"><span data-stu-id="21fd1-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="21fd1-130">Il percorso e il nome del file sono seguiti da una virgola (,) e un trattino (-), seguiti dall'ID nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="21fd1-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="21fd1-131">Se il modulo non dispone di una tabella di stringhe, questa voce può essere semplicemente la stringa del nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="21fd1-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="21fd1-132">Se si usa solo la stringa del nome visualizzato anziché una tabella di stringhe, il nome non si adatta alla lingua di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="21fd1-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="21fd1-133">**Infotip**.</span><span class="sxs-lookup"><span data-stu-id="21fd1-133">**InfoTip**.</span></span> <span data-ttu-id="21fd1-134">REG \_ sz o reg \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="21fd1-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="21fd1-135">Descrizione dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-135">A description of the Control Panel item.</span></span> <span data-ttu-id="21fd1-136">Queste informazioni vengono visualizzate in un InfoTip visualizzato quando il mouse viene posizionato sull'icona dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="21fd1-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="21fd1-137">La sintassi è identica a quella usata per LocalizedString, inclusa la possibilità di fornire semplicemente una stringa anziché un riferimento a una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="21fd1-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="21fd1-138">**System. ApplicationName**.</span><span class="sxs-lookup"><span data-stu-id="21fd1-138">**System.ApplicationName**.</span></span> <span data-ttu-id="21fd1-139">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="21fd1-139">REG\_SZ.</span></span> <span data-ttu-id="21fd1-140">Nome canonico dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="21fd1-140">The canonical name of the item.</span></span> <span data-ttu-id="21fd1-141">Il comando del modulo `control.exe /name System.ApplicationName` apre l'elemento, ad esempio `control.exe /name MyCorporation.MySettings` .</span><span class="sxs-lookup"><span data-stu-id="21fd1-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="21fd1-142">Per ulteriori informazioni sull'utilizzo di Control.exe, vedere [esecuzione di elementi del pannello di controllo](executing-control-panel-items.md) .</span><span class="sxs-lookup"><span data-stu-id="21fd1-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="21fd1-143">**System. controlpanel. Category**.</span><span class="sxs-lookup"><span data-stu-id="21fd1-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="21fd1-144">REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="21fd1-144">REG\_SZ.</span></span> <span data-ttu-id="21fd1-145">Valore che dichiara le categorie del pannello di controllo in cui viene visualizzato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="21fd1-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="21fd1-146">Più categorie sono separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="21fd1-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="21fd1-147">Nel caso dell'esempio precedente, la voce specifica che l'elemento **impostazioni personali** dovrebbe essere visualizzato nelle categorie **aspetto e personalizzazione** e **programmi** .</span><span class="sxs-lookup"><span data-stu-id="21fd1-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="21fd1-148">Vedere [assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md) per i valori di categoria possibili.</span><span class="sxs-lookup"><span data-stu-id="21fd1-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="21fd1-149">**System. software. TasksFileUrl**.</span><span class="sxs-lookup"><span data-stu-id="21fd1-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="21fd1-150">REG \_ sz o reg \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="21fd1-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="21fd1-151">Percorso del file XML che definisce i [collegamenti alle attività](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="21fd1-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="21fd1-152">Può trattarsi di un percorso di file diretto, come illustrato nell'esempio, oppure di una risorsa incorporata specificata come nome di modulo e ID di risorsa, ad esempio "% ProgramFiles% \\ \\ \\MyApp.exe MyApp,-31".</span><span class="sxs-lookup"><span data-stu-id="21fd1-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="21fd1-153">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="21fd1-153">Step 4:</span></span>

<span data-ttu-id="21fd1-154">Nella stessa sottochiave GUID aggiungere la sottochiave seguente al registro di sistema per specificare il percorso del file che contiene l'icona e l'ID risorsa dell'immagine all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="21fd1-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="21fd1-155">Si noti che, mentre la sintassi è altrimenti simile alle voci LocalizedString e InfoTip descritte in precedenza, nessun carattere ' @' viene utilizzato come prefisso nella \_ voce reg SZ o reg \_ expand \_ SZ che specifica il percorso.</span><span class="sxs-lookup"><span data-stu-id="21fd1-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="21fd1-156">Passaggio 5:</span><span class="sxs-lookup"><span data-stu-id="21fd1-156">Step 5:</span></span>

<span data-ttu-id="21fd1-157">Aggiungere al registro di sistema le informazioni seguenti per fornire il comando chiamato dal sistema quando l'utente apre il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="21fd1-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="21fd1-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21fd1-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21fd1-159">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="21fd1-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="21fd1-160">Come registrare gli elementi del pannello di controllo DLL</span><span class="sxs-lookup"><span data-stu-id="21fd1-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



