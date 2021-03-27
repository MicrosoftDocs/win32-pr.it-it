---
description: Questo argomento illustra come creare nuovi tipi di file e come associare l'app al tipo di file e ad altri tipi di file ben definiti.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979743"
---
# <a name="file-types"></a><span data-ttu-id="c3195-103">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="c3195-103">File Types</span></span>

<span data-ttu-id="c3195-104">Questo argomento illustra come creare nuovi tipi di file e come associare l'app al tipo di file e ad altri tipi di file ben definiti.</span><span class="sxs-lookup"><span data-stu-id="c3195-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="c3195-105">I file con un'estensione del nome file comune condivisa (doc, HTML e così via) sono dello stesso *tipo*.</span><span class="sxs-lookup"><span data-stu-id="c3195-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="c3195-106">Se ad esempio si crea un nuovo editor di testo, è possibile usare il tipo di file con estensione txt esistente.</span><span class="sxs-lookup"><span data-stu-id="c3195-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="c3195-107">In altri casi, potrebbe essere necessario creare un nuovo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="c3195-108">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c3195-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c3195-109">Tipi di file pubblici e privati</span><span class="sxs-lookup"><span data-stu-id="c3195-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="c3195-110">Registrazione di un tipo di file</span><span class="sxs-lookup"><span data-stu-id="c3195-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="c3195-111">Impostazione degli attributi facoltativi delle sottochiavi e dell'estensione del tipo di file</span><span class="sxs-lookup"><span data-stu-id="c3195-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="c3195-112">Eliminazione delle informazioni del registro di sistema durante la disinstallazione</span><span class="sxs-lookup"><span data-stu-id="c3195-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="c3195-113">Tipi di file che supportano i metadati aperti</span><span class="sxs-lookup"><span data-stu-id="c3195-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="c3195-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3195-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="c3195-115">Ulteriori informazioni sono disponibili negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3195-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="c3195-116">Come scegliere un'estensione del tipo di file</span><span class="sxs-lookup"><span data-stu-id="c3195-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="c3195-117">Come definire gli attributi del tipo di file</span><span class="sxs-lookup"><span data-stu-id="c3195-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   [<span data-ttu-id="c3195-118">Come includere un'applicazione nella finestra di dialogo Apri con</span><span class="sxs-lookup"><span data-stu-id="c3195-118">How To Include an Application on the Open with Dialog Box</span></span>](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [<span data-ttu-id="c3195-119">Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati</span><span class="sxs-lookup"><span data-stu-id="c3195-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="c3195-120">Tipi di file pubblici e privati</span><span class="sxs-lookup"><span data-stu-id="c3195-120">Public and Private File Types</span></span>

<span data-ttu-id="c3195-121">I tipi di file pubblici sono noti anche come tipi più diffusi o controversi perché le applicazioni in competizione potrebbero voler essere associate a questi tipi di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="c3195-122">Le caratteristiche dei tipi di file pubblici includono:</span><span class="sxs-lookup"><span data-stu-id="c3195-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="c3195-123">Vengono in genere definiti da corpi di standard e/o vengono promossi dalle organizzazioni che lo definiscono come formati di interscambio.</span><span class="sxs-lookup"><span data-stu-id="c3195-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="c3195-124">Spesso vengono scambiati tra computer e utenti per diversi scopi.</span><span class="sxs-lookup"><span data-stu-id="c3195-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="c3195-125">Devono essere supportate su molte piattaforme diverse.</span><span class="sxs-lookup"><span data-stu-id="c3195-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="c3195-126">È probabile che le applicazioni di più fornitori li gestiscano.</span><span class="sxs-lookup"><span data-stu-id="c3195-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="c3195-127">Alcuni esempi di tipi di file che sono considerati pubblici sono i tipi di file immagine. png,. gif,. jpg e. bmp e i tipi audio. wav,. mp3 e. au.</span><span class="sxs-lookup"><span data-stu-id="c3195-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="c3195-128">A differenza dei tipi di file pubblici, i tipi di file privati o proprietari hanno in genere un formato implementato e compreso da una sola applicazione o fornitore.</span><span class="sxs-lookup"><span data-stu-id="c3195-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="c3195-129">Di conseguenza, i tipi di file privati in genere non sono soggetti a conflitti tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c3195-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="c3195-130">Alcuni tipi di file possono essere avviati come tipi di file privati, ma in seguito diventano tipi di file pubblici.</span><span class="sxs-lookup"><span data-stu-id="c3195-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="c3195-131">Windows non distingue tra i tipi di file pubblici e privati.</span><span class="sxs-lookup"><span data-stu-id="c3195-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="c3195-132">La distinzione è rilevante solo per prendere decisioni sulla scelta della registrazione del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="c3195-133">Registrazione di un tipo di file</span><span class="sxs-lookup"><span data-stu-id="c3195-133">Registering a File Type</span></span>

<span data-ttu-id="c3195-134">Per associare il tipo di file a un'applicazione esistente, individuare il ProgID dell'applicazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c3195-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="c3195-135">Per associare il tipo di file a una nuova applicazione, definire un ProgID per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3195-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="c3195-136">Per informazioni sulla definizione di un nuovo ProgID, vedere [identificatori a livello di codice](fa-progids.md).</span><span class="sxs-lookup"><span data-stu-id="c3195-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="c3195-137">Le sottochiavi di estensione del nome file hanno il formato generale seguente: *estensione* = *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="c3195-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="c3195-138">Le sottochiavi dell'estensione del nome file sono archiviate nel sottoalbero **\_ \_ radice delle classi HKEY** .</span><span class="sxs-lookup"><span data-stu-id="c3195-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="c3195-139">Quando si creano sottochiavi di tipo file nel registro di sistema, è importante includere il punto principale (.).</span><span class="sxs-lookup"><span data-stu-id="c3195-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="c3195-140">Ad esempio, se si desidera che un tipo di file con estensione. MYP e il file con estensione MYP lungo da aprire con un'applicazione denominata programma, utilizzare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="c3195-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="c3195-141">Come illustrato nell'esempio precedente, se si registra anche un'estensione di file breve (MYP), è necessario creare una sottochiave per l'estensione lunga (file con estensione MYP).</span><span class="sxs-lookup"><span data-stu-id="c3195-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="c3195-142">Per altre informazioni, vedere [gestori di tipi di file](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c3195-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="c3195-143">Impostazione degli attributi facoltativi delle sottochiavi e dell'estensione del tipo di file</span><span class="sxs-lookup"><span data-stu-id="c3195-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="c3195-144">Le voci dell'estensione del tipo di file nel registro di sistema includono diverse sottochiavi e attributi facoltativi.</span><span class="sxs-lookup"><span data-stu-id="c3195-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="c3195-145">Nella tabella seguente vengono descritte le voci dell'estensione del tipo di file utilizzate dalle associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="c3195-146">Tutti i valori sono di tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="c3195-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="c3195-147">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c3195-147">Registry entry</span></span>  | <span data-ttu-id="c3195-148">Azione</span><span class="sxs-lookup"><span data-stu-id="c3195-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3195-149">Predefinito</span><span class="sxs-lookup"><span data-stu-id="c3195-149">Default</span></span>         | <span data-ttu-id="c3195-150">Impostare il valore predefinito della sottochiave Extension sul ProgID a cui è collegato.</span><span class="sxs-lookup"><span data-stu-id="c3195-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c3195-151">Tipo di contenuto</span><span class="sxs-lookup"><span data-stu-id="c3195-151">Content Type</span></span>    | <span data-ttu-id="c3195-152">Impostare il valore del tipo di contenuto sul tipo di contenuto MIME del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c3195-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="c3195-153">OpenWithList</span></span>    | <span data-ttu-id="c3195-154">Non usare.</span><span class="sxs-lookup"><span data-stu-id="c3195-154">Do not use.</span></span> <span data-ttu-id="c3195-155">Questa sottochiave contiene una o più sottochiavi dell'applicazione per le applicazioni visualizzate nella voce della finestra di dialogo **Apri con** per il tipo di file ed è destinata solo alle applicazioni exe nei sistemi operativi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3195-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="c3195-156">In alternativa, usare OpenWithProgIds.</span><span class="sxs-lookup"><span data-stu-id="c3195-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="c3195-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="c3195-157">OpenWithProgIds</span></span> | <span data-ttu-id="c3195-158">Questa sottochiave contiene un elenco di ProgID alternativi per questo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="c3195-159">I programmi per questi ProgID vengono visualizzati nel menu **Apri con** e sono disponibili come app di Windows Store predefinite per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c3195-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="c3195-160">Ogni volta che un'applicazione acquisisce questo tipo di file modificando il valore predefinito, deve aggiungere anche una voce a questo elenco.</span><span class="sxs-lookup"><span data-stu-id="c3195-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="c3195-161">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c3195-161">PerceivedType</span></span>   | <span data-ttu-id="c3195-162">Impostare il valore PerceivedType su PerceivedType a cui appartiene il file, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="c3195-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="c3195-163">Questa stringa non viene utilizzata dalle versioni di Windows precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3195-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="c3195-164">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione delle applicazioni e dei tipi percepiti](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="c3195-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="c3195-165">Il formato generale di una sottochiave di estensione del nome file è il seguente.</span><span class="sxs-lookup"><span data-stu-id="c3195-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="c3195-166">Tutti i tipi di voce sono di tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="c3195-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="c3195-167">Importanti considerazioni sui tipi di file includono:</span><span class="sxs-lookup"><span data-stu-id="c3195-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="c3195-168">Il sottoalbero **\_ \_ radice delle classi HKEY** è una visualizzazione formata unendo le classi software **\_ \_ dell'utente corrente di HKEY** \\  \\  e le classi software **\_ del \_ computer locale HKEY** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="c3195-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="c3195-169">In generale, **la \_ \_ radice delle classi HKEY** è destinata a essere letta da ma non scritta.</span><span class="sxs-lookup"><span data-stu-id="c3195-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="c3195-170">Per altre informazioni, vedere l' [articolo \_ \_ radice delle classi HKEY](../sysinfo/hkey-classes-root-key.md) .</span><span class="sxs-lookup"><span data-stu-id="c3195-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="c3195-171">Per registrare un tipo di file a livello globale in un determinato computer, creare una voce per il tipo di file nella **\_ \_** \\  \\ sottochiave **classi** software del computer locale HKEY.</span><span class="sxs-lookup"><span data-stu-id="c3195-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="c3195-172">Per rendere visibile la registrazione di un tipo di file solo all'utente corrente, creare una voce per il tipo di file nella sottochiave classi software **\_ \_ dell'utente corrente di HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="c3195-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="c3195-173">Un'applicazione può fornire la propria implementazione di un verbo, ad esempio Open o Play, come illustrato nell'esempio di registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="c3195-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="c3195-174">Le sottochiavi della sottochiave del verbo includono la riga di comando e il metodo Drop target: **Command** e **DropTarget**.</span><span class="sxs-lookup"><span data-stu-id="c3195-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="c3195-175">Quando si crea o si modifica un'associazione di file, è importante notificare al sistema che è stata apportata una modifica.</span><span class="sxs-lookup"><span data-stu-id="c3195-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="c3195-176">Eseguire questa operazione chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) e specificando l'evento **SHCNE \_ ASSOCCHANGED** .</span><span class="sxs-lookup"><span data-stu-id="c3195-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="c3195-177">Se non si chiama **SHChangeNotify**, è possibile che la modifica non venga riconosciuta fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c3195-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="c3195-178">Per recuperare le informazioni del registro di sistema relative a un'associazione di file, utilizzare l'interfaccia [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="c3195-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="c3195-179">Per uno scenario che illustra questa procedura, vedere [scenario di esempio di associazione di file](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="c3195-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="c3195-180">Le sottochiavi del registro di sistema per le **applicazioni** e i **percorsi delle app** vengono usate per registrare e controllare il comportamento del sistema per conto delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c3195-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="c3195-181">Per informazioni più dettagliate su questa funzionalità, vedere [registrazione dell'applicazione](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="c3195-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="c3195-182">Eliminazione delle informazioni del registro di sistema durante la disinstallazione</span><span class="sxs-lookup"><span data-stu-id="c3195-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="c3195-183">Quando si disinstalla un'applicazione, i ProgID e la maggior parte delle altre informazioni di registro associate a tale applicazione devono essere eliminati come parte della disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="c3195-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="c3195-184">Tuttavia, le applicazioni che hanno assunto la proprietà di un tipo di file (impostando il valore predefinito della sottochiave **\_ \_ radice**. Extension del tipo di file Hkey \\  per il ProgID dell'applicazione) non devono tentare di rimuovere tale valore durante la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="c3195-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="c3195-185">Se si lasciano i dati per il valore predefinito, si evita la difficoltà di determinare se un'altra applicazione ha assunto la proprietà del tipo di file e sovrascritto il valore predefinito dopo l'installazione dell'applicazione originale.</span><span class="sxs-lookup"><span data-stu-id="c3195-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="c3195-186">Windows rispetta il valore predefinito solo se il ProgID individuato è un ProgID registrato.</span><span class="sxs-lookup"><span data-stu-id="c3195-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="c3195-187">Se il ProgID viene annullata, viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c3195-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="c3195-188">Si noti che altre informazioni sulla proprietà dei tipi di file vengono archiviate nel sottoalbero dell' **\_ \_ utente corrente di HKEY** e vengono usate solo quando l'applicazione a cui fa riferimento è registrata.</span><span class="sxs-lookup"><span data-stu-id="c3195-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="c3195-189">Pertanto, questi dati non devono essere rimossi durante la disinstallazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3195-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="c3195-190">Come esempio, di seguito viene illustrato lo stato del registro di sistema prima della disinstallazione di un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="c3195-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="c3195-191">Di seguito viene illustrato lo stato delle stesse voci del registro di sistema dopo la disinstallazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3195-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="c3195-192">Tipi di file che supportano i metadati aperti</span><span class="sxs-lookup"><span data-stu-id="c3195-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="c3195-193">In Windows 7 e versioni successive, i tipi di file seguenti supportano i metadati aperti.</span><span class="sxs-lookup"><span data-stu-id="c3195-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="c3195-194">Tipo file</span><span class="sxs-lookup"><span data-stu-id="c3195-194">File type</span></span>                                                               | <span data-ttu-id="c3195-195">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="c3195-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c3195-196">Documenti di Office 2007</span><span class="sxs-lookup"><span data-stu-id="c3195-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="c3195-197">. docx,. xlsx,. pptx</span><span class="sxs-lookup"><span data-stu-id="c3195-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="c3195-198">Documenti di Office 97-2003</span><span class="sxs-lookup"><span data-stu-id="c3195-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="c3195-199">DOC, xls, PPT</span><span class="sxs-lookup"><span data-stu-id="c3195-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="c3195-200">Ricerca salvata</span><span class="sxs-lookup"><span data-stu-id="c3195-200">Saved Search</span></span>                                                            | <span data-ttu-id="c3195-201">. search-ms</span><span class="sxs-lookup"><span data-stu-id="c3195-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="c3195-202">Formati basati su Windows Media (contenitore ASF (Advanced Streaming Format)</span><span class="sxs-lookup"><span data-stu-id="c3195-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="c3195-203">. wmv,. WMA</span><span class="sxs-lookup"><span data-stu-id="c3195-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="c3195-204">MP4 (gestore proprietà)</span><span class="sxs-lookup"><span data-stu-id="c3195-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="c3195-205">. MP4,. m4a,. m4v,. mp4v,. M4P,. m4b,. 3GP,. 3GPP,. 3gp2,. MOV</span><span class="sxs-lookup"><span data-stu-id="c3195-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c3195-206">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3195-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3195-207">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="c3195-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="c3195-208">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="c3195-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="c3195-209">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="c3195-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="c3195-210">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="c3195-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="c3195-211">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="c3195-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="c3195-212">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="c3195-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="c3195-213">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="c3195-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="c3195-214">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="c3195-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
