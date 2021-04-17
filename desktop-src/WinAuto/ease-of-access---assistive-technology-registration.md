---
title: Registrazione facilitata della tecnologia di accesso facilitato
description: Questo articolo illustra come registrare un'applicazione di accessibilità con la facilità di accesso al centro. Viene inoltre illustrato come adattare l'applicazione di accessibilità in modo che funzioni correttamente con il desktop protetto.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300183"
---
# <a name="ease-of-access---assistive-technology-registration"></a><span data-ttu-id="9a03b-104">Registrazione facilitata della tecnologia di accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="9a03b-104">Ease of Access   Assistive Technology Registration</span></span>

<span data-ttu-id="9a03b-105">Questo articolo illustra come registrare un'applicazione di accessibilità con la facilità di accesso al centro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-105">This article explains how to register an accessibility application with the Ease of Access Center.</span></span> <span data-ttu-id="9a03b-106">Viene inoltre illustrato come adattare l'applicazione di accessibilità in modo che funzioni correttamente con il desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-106">It also explains how to tailor your accessibility application so it works well with the secure desktop.</span></span>

<span data-ttu-id="9a03b-107">Il Centro accesso facilitato è un'applicazione del pannello di controllo per Microsoft Windows che riunisce le funzionalità per l'accessibilità e la semplicità d'uso.</span><span class="sxs-lookup"><span data-stu-id="9a03b-107">The Ease of Access Center is a Control Panel application for Microsoft Windows brings together functionality for accessibility and ease of use.</span></span> <span data-ttu-id="9a03b-108">Grazie alla facilità di accesso al centro, gli utenti possono configurare i computer in base alle proprie esigenze fisiche e cognitive.</span><span class="sxs-lookup"><span data-stu-id="9a03b-108">By using the Ease of Access Center, users can configure their computers to suit their physical and cognitive needs.</span></span>

<span data-ttu-id="9a03b-109">Una funzione del Centro accesso facilitato è aiutare gli utenti a avviare applicazioni di accessibilità, tra cui Assistente vocale, tastiera su schermo e lente di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="9a03b-109">One function of the Ease of Access Center is to help users launch accessibility applications, including Narrator, On-Screen Keyboard, and Magnifier.</span></span> <span data-ttu-id="9a03b-110">Le applicazioni registrate di terze parti vengono visualizzate anche nel centro di accesso facilitato e possono essere avviate direttamente da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-110">Registered third-party applications also appear in the Ease of Access Center and can be launched directly from there.</span></span>

<span data-ttu-id="9a03b-111">Le applicazioni di accessibilità devono funzionare senza problemi con il desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-111">Accessibility applications need to work smoothly with the secure desktop.</span></span> <span data-ttu-id="9a03b-112">Il desktop sicuro è l'interfaccia utente visualizzata quando il computer è bloccato (al momento dell'accesso o quando l'utente ha bloccato il desktop) e quando all'utente viene richiesto di consentire un'azione potenzialmente non sicura.</span><span class="sxs-lookup"><span data-stu-id="9a03b-112">The secure desktop is the user interface that appears when the computer is locked (at log-on or when the user has locked the desktop), and when the user is prompted to allow a potentially unsafe action.</span></span> <span data-ttu-id="9a03b-113">Per motivi di sicurezza, Windows pone limiti a software di terze parti in esecuzione sul desktop sicuro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-113">For security reasons, Windows places limits on third-party software running on the secure desktop.</span></span> <span data-ttu-id="9a03b-114">Se si vuole che l'applicazione di accessibilità venga eseguita sul desktop protetto, è necessario registrare l'applicazione con la facilità di accesso al centro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-114">If you want your accessibility application to run on the secure desktop, you need to register the application with the Ease of Access Center.</span></span>

## <a name="registering-with-the-ease-of-access-center"></a><span data-ttu-id="9a03b-115">Registrazione con la facilità di accesso al centro</span><span class="sxs-lookup"><span data-stu-id="9a03b-115">Registering with the Ease of Access Center</span></span>

<span data-ttu-id="9a03b-116">Le applicazioni di accessibilità si registrano con la facilità di accesso al centro creando una o più chiavi del registro di sistema durante l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-116">Accessibility applications register with the Ease of Access Center by creating one or more registry keys when the application is installed.</span></span> <span data-ttu-id="9a03b-117">Nella tabella seguente sono elencate le informazioni contenute nelle chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9a03b-117">The following table lists the information contained in the registry keys.</span></span>



| <span data-ttu-id="9a03b-118">Nome</span><span class="sxs-lookup"><span data-stu-id="9a03b-118">Name</span></span>                        | <span data-ttu-id="9a03b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a03b-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="9a03b-120">Obbligatorio/facoltativo</span><span class="sxs-lookup"><span data-stu-id="9a03b-120">Mandatory/Optional</span></span> | <span data-ttu-id="9a03b-121">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="9a03b-121">Language</span></span>      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| <span data-ttu-id="9a03b-122">Nome dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9a03b-122">Application Name</span></span>            | <span data-ttu-id="9a03b-123">Nome dell'applicazione, che si trova in un file di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a03b-123">The name of the application, which is in a resource file.</span></span> <span data-ttu-id="9a03b-124">Questo valore del registro di sistema contiene una stringa in un formato specificato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-124">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="9a03b-125">Potrebbe trattarsi di una versione localizzata del nome dell'applicazione, se l'applicazione è localizzata in lingue diverse dall'inglese.</span><span class="sxs-lookup"><span data-stu-id="9a03b-125">This could be a localized version of the application name, if the application is localized in languages other than English.</span></span> <span data-ttu-id="9a03b-126">Il nome viene visualizzato nel centro accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-126">The name appears in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="9a03b-127">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9a03b-127">Mandatory</span></span>          | <span data-ttu-id="9a03b-128">Localizzata</span><span class="sxs-lookup"><span data-stu-id="9a03b-128">Localized</span></span>     |
| <span data-ttu-id="9a03b-129">ATEx</span><span class="sxs-lookup"><span data-stu-id="9a03b-129">ATExe</span></span>                       | <span data-ttu-id="9a03b-130">Nome del file eseguibile dell'applicazione o dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="9a03b-130">The name of the application executable file or image.</span></span> <span data-ttu-id="9a03b-131">Windows utilizza questo valore per determinare se l'applicazione di accessibilità è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-131">Windows uses this value to determine whether the accessibility application is running.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="9a03b-132">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9a03b-132">Mandatory</span></span>          | <span data-ttu-id="9a03b-133">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-133">Not localized</span></span> |
| <span data-ttu-id="9a03b-134">CopySettingsToLockedDesktop</span><span class="sxs-lookup"><span data-stu-id="9a03b-134">CopySettingsToLockedDesktop</span></span> | <span data-ttu-id="9a03b-135">Valore **DWORD** che indica se copiare le impostazioni dell'applicazione di accessibilità sul desktop bloccato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-135">A **DWORD** value that indicates whether to copy the accessibility application's settings to the locked desktop.</span></span><br/> <span data-ttu-id="9a03b-136">Se questo valore è 1, l'applicazione può scrivere le impostazioni in un percorso nel registro utenti e Windows copia le impostazioni nello stesso percorso nel registro utenti per il desktop bloccato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-136">If this value is 1, the application can write settings to a location in the user registry, and Windows copies the settings to the same location in the user registry for the locked desktop.</span></span> <span data-ttu-id="9a03b-137">Ciò consente all'applicazione di salvare in modo permanente il proprio stato dal desktop "normale" al desktop bloccato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-137">This enables the application to persist its state from the "normal" desktop to the locked desktop.</span></span><br/>                                                                                                                                                             | <span data-ttu-id="9a03b-138">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="9a03b-138">Optional</span></span>           | <span data-ttu-id="9a03b-139">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-139">Not localized</span></span> |
| <span data-ttu-id="9a03b-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a03b-140">Description</span></span>                 | <span data-ttu-id="9a03b-141">Breve descrizione dell'applicazione, da un file di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a03b-141">A brief description of the application, from a resource file.</span></span> <span data-ttu-id="9a03b-142">Questo valore del registro di sistema contiene una stringa in un formato specificato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-142">This registry value contains a string in a specified format.</span></span> <span data-ttu-id="9a03b-143">Potrebbe trattarsi di una versione localizzata della descrizione, se l'applicazione è localizzata in lingue diverse dall'inglese.</span><span class="sxs-lookup"><span data-stu-id="9a03b-143">This could be a localized version of the description, if the application is localized in languages other than English.</span></span> <span data-ttu-id="9a03b-144">La lunghezza di questa stringa deve essere inferiore a 512 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9a03b-144">The length of this string must be less than 512 characters.</span></span><br/> <span data-ttu-id="9a03b-145">La descrizione viene visualizzata nel centro di accesso facilitato per fornire informazioni aggiuntive sull'applicazione di accessibilità all'utente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-145">The description appears in the Ease of Access Center to provide additional information about the accessibility application to the user.</span></span><br/> <span data-ttu-id="9a03b-146">Questo valore può essere usato anche per notificare all'utente che l'applicazione non viene usata sul desktop sicuro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-146">This value can also be used to notify the user that the application is not used on the secure desktop.</span></span><br/>      | <span data-ttu-id="9a03b-147">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9a03b-147">Mandatory</span></span>          | <span data-ttu-id="9a03b-148">Localizzata</span><span class="sxs-lookup"><span data-stu-id="9a03b-148">Localized</span></span>     |
| <span data-ttu-id="9a03b-149">Profilo</span><span class="sxs-lookup"><span data-stu-id="9a03b-149">Profile</span></span>                     | <span data-ttu-id="9a03b-150">Breve frammento di codice XML che specifica le sistemazioni fornite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-150">A short piece of XML that specifies the accommodations that the application provides.</span></span> <span data-ttu-id="9a03b-151">Garantisce che l'applicazione venga visualizzata sotto la categoria corretta nel centro accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-151">It ensures that the application appears under the correct category in the Ease of Access Center.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="9a03b-152">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9a03b-152">Mandatory</span></span>          | <span data-ttu-id="9a03b-153">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-153">Not localized</span></span> |
| <span data-ttu-id="9a03b-154">PassiveAutoStartBehavior</span><span class="sxs-lookup"><span data-stu-id="9a03b-154">PassiveAutoStartBehavior</span></span>    | <p><span data-ttu-id="9a03b-155">Valore **DWORD** che indica se il comportamento di avvio automatico legacy è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-155">A **DWORD** value that indicates whether legacy auto-start behavior is enabled.</span></span></p><p><span data-ttu-id="9a03b-156">Il valore predefinito è 0, che indica che un oggetto AT richiede un comportamento di avvio automatico legacy.</span><span class="sxs-lookup"><span data-stu-id="9a03b-156">The default value is 0, which indicates that an AT requires legacy auto-start behavior.</span></span> <span data-ttu-id="9a03b-157">In questo modo, l'impostazione "avvia dopo l'accesso" per l'oggetto in verrà archiviata nella configurazione guidata e nel pannello di controllo (vedere **Pannello di controllo-> facilità di accesso-> facilità di accesso al centro-> modificare le impostazioni di accesso**) e avvia automaticamente il dopo UAC e la schermata di blocco.</span><span class="sxs-lookup"><span data-stu-id="9a03b-157">This  causes the “Start after sign-in” setting for that AT to be checked in the Out Of Box Experience (OOBE) and Control Panel (see **Control Panel -> Ease of Access -> Ease of Access Center -> Change sign-in settings**), and automatically starts the AT after UAC and lock-screen.</span></span></p><p><span data-ttu-id="9a03b-158">Il valore 1 indica che in deve essere utilizzato il nuovo comportamento di avvio automatico in cui l'impostazione "avvia dopo l'accesso" in non viene archiviata nella configurazione guidata e nel pannello di controllo e viene automaticamente avviata una volta per ogni sessione utente (all'accesso) solo se viene selezionata l'impostazione "avvia dopo l'accesso".</span><span class="sxs-lookup"><span data-stu-id="9a03b-158">A value of 1 indicates that the AT should use the new auto-start behavior where the “Start after sign-in” setting for that AT is not checked in the Out Of Box Experience (OOBE) and Control Panel, and the AT is automatically started once per user session (at login) only if the “start after sign-in” setting is checked.</span></span></p>                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="9a03b-159">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="9a03b-159">Optional</span></span>          | <span data-ttu-id="9a03b-160">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-160">Not localized</span></span> |
| <span data-ttu-id="9a03b-161">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="9a03b-161">SecureDesktopAccommodation</span></span>  | <span data-ttu-id="9a03b-162">Nome di un'applicazione di accessibilità alternativa da eseguire sul desktop protetto al posto di questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-162">The name of an alternate accessibility application to run on the secure desktop in the place of this application.</span></span> <span data-ttu-id="9a03b-163">L'alternativa può essere un'applicazione diversa, una versione diversa della stessa applicazione, una delle applicazioni di accessibilità inclusa in Windows o "None" se non si desidera eseguire alcuna applicazione di accessibilità sul desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-163">The alternate can be a different application, a different version of the same application, one of the accessibility applications that is included in Windows, or "none" if you do not want to run any accessibility application on the secure desktop.</span></span> <br/>                                                                                                                                                                                                               | <span data-ttu-id="9a03b-164">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="9a03b-164">Optional</span></span>           | <span data-ttu-id="9a03b-165">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-165">Not localized</span></span> |
| <span data-ttu-id="9a03b-166">Profilo semplice</span><span class="sxs-lookup"><span data-stu-id="9a03b-166">Simple Profile</span></span>              | <span data-ttu-id="9a03b-167">Valore che descrive come classificare l'applicazione in una parola o due:, ad esempio, una tastiera a schermo, una lente di ingrandimento o una tastiera sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="9a03b-167">A value that describes how to classify the application in a word or two: Screen reader, Magnifier, or On-screen keyboard, for example.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="9a03b-168">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9a03b-168">Mandatory</span></span>          | <span data-ttu-id="9a03b-169">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-169">Not localized</span></span> |
| <span data-ttu-id="9a03b-170">StartExe</span><span class="sxs-lookup"><span data-stu-id="9a03b-170">StartExe</span></span>                    | <span data-ttu-id="9a03b-171">Percorso completo del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="9a03b-171">The full path of the executable.</span></span> <span data-ttu-id="9a03b-172">Questo valore viene utilizzato per avviare l'applicazione di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="9a03b-172">This value is used to launch the accessibility application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="9a03b-173">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9a03b-173">Mandatory</span></span>          | <span data-ttu-id="9a03b-174">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-174">Not localized</span></span> |
| <span data-ttu-id="9a03b-175">StartParams</span><span class="sxs-lookup"><span data-stu-id="9a03b-175">StartParams</span></span>                 | <span data-ttu-id="9a03b-176">Argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9a03b-176">Command-line arguments.</span></span> <span data-ttu-id="9a03b-177">Questi valori vengono usati insieme a StartExe per avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-177">These values are used along with StartExe to start the application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="9a03b-178">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="9a03b-178">Optional</span></span>           | <span data-ttu-id="9a03b-179">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-179">Not localized</span></span> |
| <span data-ttu-id="9a03b-180">TerminateOnDesktopSwitch</span><span class="sxs-lookup"><span data-stu-id="9a03b-180">TerminateOnDesktopSwitch</span></span>    | <span data-ttu-id="9a03b-181">Valore **DWORD** che specifica il modo in cui l'applicazione di accessibilità risponde alle transizioni verso o dal desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-181">A **DWORD** value that specifies how the accessibility application responds to transitions to or from the secure desktop.</span></span><br/> <span data-ttu-id="9a03b-182">Se questo valore non esiste o è 1, Windows termina e riavvia l'applicazione a ogni transizione da o verso il desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-182">If this value does not exist or is 1, Windows terminates and restarts the application on each transition to or from the secure desktop.</span></span> <span data-ttu-id="9a03b-183">Comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="9a03b-183">This is the default behavior.</span></span><br/> <span data-ttu-id="9a03b-184">Se questo valore è 0, Windows non termina l'applicazione di accessibilità su una transizione desktop.</span><span class="sxs-lookup"><span data-stu-id="9a03b-184">If this value is 0, Windows does not terminate the accessibility application on a desktop transition.</span></span> <span data-ttu-id="9a03b-185">L'applicazione continuerà a essere eseguita sul desktop precedente e Windows avvierà una nuova istanza sul nuovo desktop se un'istanza non è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-185">The application continues to run on the previous desktop, and Windows starts a new instance on the new desktop if an instance is not already running there.</span></span><br/> | <span data-ttu-id="9a03b-186">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="9a03b-186">Optional</span></span>           | <span data-ttu-id="9a03b-187">Non localizzato</span><span class="sxs-lookup"><span data-stu-id="9a03b-187">Not localized</span></span> |


 

### <a name="localization"></a><span data-ttu-id="9a03b-188">Localizzazione</span><span class="sxs-lookup"><span data-stu-id="9a03b-188">Localization</span></span>

<span data-ttu-id="9a03b-189">I valori del registro di sistema del nome e della descrizione dell'applicazione devono essere localizzabili per supportare MUI (Multilingual User Interface).</span><span class="sxs-lookup"><span data-stu-id="9a03b-189">The registry values of Application Name and Description need to be localizable to support Multilingual User Interface (MUI).</span></span>

<span data-ttu-id="9a03b-190">Queste stringhe hanno il formato seguente, dove le parentesi angolari indicano gli elementi obbligatori e le parentesi quadre indicano un elemento facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9a03b-190">These strings are in the following format, where angle brackets signify required elements and square brackets signify an optional element.</span></span>

<span data-ttu-id="9a03b-191">*@ <ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*</span><span class="sxs-lookup"><span data-stu-id="9a03b-191">*@<ResDllPath\\ResDLLFilename>,-<resID>\[;<comment>\]*</span></span>

<span data-ttu-id="9a03b-192">*<ResDllPath \\ ResDLLFilename>* è il percorso della dll della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-192">*<ResDllPath\\ResDLLFilename>* is the path to the resource DLL.</span></span> <span data-ttu-id="9a03b-193">Il percorso può contenere variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-193">The path can contain environmental variables.</span></span>

<span data-ttu-id="9a03b-194">*<resID>* ID di risorsa della stringa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-194">*<resID>* is the resource ID for the string.</span></span>

<span data-ttu-id="9a03b-195">il *\[ Commento \]* contiene commenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="9a03b-195">*\[comment\]* contains any optional comments.</span></span>

<span data-ttu-id="9a03b-196">Ecco un esempio:</span><span class="sxs-lookup"><span data-stu-id="9a03b-196">Here is an example:</span></span>


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



<span data-ttu-id="9a03b-197">Per ulteriori informazioni su MUI, vedere [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9a03b-197">For more information about MUI, see [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).</span></span>

### <a name="hci-profile"></a><span data-ttu-id="9a03b-198">Profilo HCI</span><span class="sxs-lookup"><span data-stu-id="9a03b-198">HCI Profile</span></span>

<span data-ttu-id="9a03b-199">Il profilo di interazione human computer (HCI) è un modo per determinare quali sistemazioni fornire in base alle esigenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-199">The Human Computer Interaction (HCI) profile is a way to determine what accommodations to provide based on the needs of the user.</span></span> <span data-ttu-id="9a03b-200">Le applicazioni per l'accessibilità dovrebbero registrare informazioni sul tipo di disabilità che l'applicazione può supportare.</span><span class="sxs-lookup"><span data-stu-id="9a03b-200">Accessibility applications should register information about the kind of disability the application helps to accommodate.</span></span>

<span data-ttu-id="9a03b-201">Il valore del registro di sistema del profilo contiene codice XML che descrive il tipo di disabilità di destinazione dell'applicazione di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="9a03b-201">The Profile registry value contains XML that describes the kind of disability targeted by the accessibility application.</span></span> <span data-ttu-id="9a03b-202">Questo XML ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="9a03b-202">This XML has the following format:</span></span>


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



<span data-ttu-id="9a03b-203">I valori validi per l'attributo **tipo di alloggio** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a03b-203">The valid values for the **Accommodation type** attribute are as follows:</span></span>

-   <span data-ttu-id="9a03b-204">visione lieve</span><span class="sxs-lookup"><span data-stu-id="9a03b-204">mild vision</span></span>
-   <span data-ttu-id="9a03b-205">visione grave</span><span class="sxs-lookup"><span data-stu-id="9a03b-205">severe vision</span></span>
-   <span data-ttu-id="9a03b-206">cognitive lieve</span><span class="sxs-lookup"><span data-stu-id="9a03b-206">mild cognitive</span></span>
-   <span data-ttu-id="9a03b-207">cognitivo grave</span><span class="sxs-lookup"><span data-stu-id="9a03b-207">severe cognitive</span></span>
-   <span data-ttu-id="9a03b-208">destrezza lieve</span><span class="sxs-lookup"><span data-stu-id="9a03b-208">mild dexterity</span></span>
-   <span data-ttu-id="9a03b-209">destrezza grave</span><span class="sxs-lookup"><span data-stu-id="9a03b-209">severe dexterity</span></span>
-   <span data-ttu-id="9a03b-210">udito lieve</span><span class="sxs-lookup"><span data-stu-id="9a03b-210">mild hearing</span></span>
-   <span data-ttu-id="9a03b-211">udito grave</span><span class="sxs-lookup"><span data-stu-id="9a03b-211">severe hearing</span></span>
-   <span data-ttu-id="9a03b-212">riconoscimento vocale lieve</span><span class="sxs-lookup"><span data-stu-id="9a03b-212">mild speech</span></span>
-   <span data-ttu-id="9a03b-213">riconoscimento vocale grave</span><span class="sxs-lookup"><span data-stu-id="9a03b-213">severe speech</span></span>

> [!Note]  
> <span data-ttu-id="9a03b-214">Per tali valori viene applicata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9a03b-214">These values are case sensitive.</span></span>

 

<span data-ttu-id="9a03b-215">Se un'applicazione di accessibilità supporta più alloggi, il valore del registro di sistema del profilo deve includere un attributo del **tipo di alloggio** per ogni alloggio.</span><span class="sxs-lookup"><span data-stu-id="9a03b-215">If an accessibility application supports multiple accommodations, the Profile registry value should include an **Accommodation type** attribute for each accommodation.</span></span>

### <a name="ease-of-access-registry-details"></a><span data-ttu-id="9a03b-216">Dettagli del registro di sistema di accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="9a03b-216">Ease of Access registry details</span></span>

<span data-ttu-id="9a03b-217">Per registrare l'applicazione di accessibilità, è necessario creare una chiave per l'applicazione nel seguente percorso del registro di sistema e popolarla con coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="9a03b-217">To register your accessibility application, you need to create a key for your application at the following registry location and populate it with name-value pairs.</span></span>

<span data-ttu-id="9a03b-218">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibilità \\ ATS\\**</span><span class="sxs-lookup"><span data-stu-id="9a03b-218">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\**</span></span>

<span data-ttu-id="9a03b-219">Assegnare un nome alla chiave del registro di sistema dell'applicazione usando il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="9a03b-219">Name your application's registry key using the following format:</span></span>

<span data-ttu-id="9a03b-220">*"CompanyName \_ ProductName \_ v \# "*</span><span class="sxs-lookup"><span data-stu-id="9a03b-220">*"CompanyName\_ProductName\_v\#"*</span></span>

<span data-ttu-id="9a03b-221">Ad esempio, "Contoso \_ Magnifier \_ v 2.0".</span><span class="sxs-lookup"><span data-stu-id="9a03b-221">For example, "Contoso\_Magnifier\_v2.0".</span></span>

<span data-ttu-id="9a03b-222">Per aggiungere i valori del registro di sistema, è necessario che il programma di installazione sia in esecuzione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="9a03b-222">To add registry values, your installation program must be running with elevated privileges.</span></span>

### <a name="secure-desktop-accommodation"></a><span data-ttu-id="9a03b-223">Secure Desktop accommodation</span><span class="sxs-lookup"><span data-stu-id="9a03b-223">Secure desktop accommodation</span></span>

<span data-ttu-id="9a03b-224">La chiave del registro di sistema **SecureDesktopAccommodation** consente di specificare il modo in cui l'applicazione di accessibilità risponde al desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-224">The **SecureDesktopAccommodation** registry key lets you specify how your accessibility application responds to the secure desktop.</span></span> <span data-ttu-id="9a03b-225">Per impostazione predefinita, la facilità di accesso al centro avvia l'applicazione sul desktop protetto se è già in esecuzione sul desktop normale o se è configurata per l'esecuzione sul desktop di accesso.</span><span class="sxs-lookup"><span data-stu-id="9a03b-225">By default, the Ease of Access Center launches your application on the secure desktop if it was already running on the normal desktop, or if it is configured to run on the logon desktop.</span></span> <span data-ttu-id="9a03b-226">Utilizzando la chiave **SecureDesktopAccommodation** , è possibile:</span><span class="sxs-lookup"><span data-stu-id="9a03b-226">By using the **SecureDesktopAccommodation** key, you can:</span></span>

-   <span data-ttu-id="9a03b-227">Specificare una versione alternativa dell'applicazione da usare sul desktop sicuro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-227">Specify an alternate version of your application for use on the secure desktop.</span></span> <span data-ttu-id="9a03b-228">Ad esempio, si potrebbe avere una versione alternativa che disabilita le funzionalità non protette o è ottimizzata per usare meno memoria e avviare più velocemente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-228">For example, you might have an alternate version that disables unsecured features, or is optimized to use less memory and launch faster.</span></span>

    <span data-ttu-id="9a03b-229">Per specificare la versione alternativa, impostare la chiave **SecureDesktopAccommodation** sul nome della versione alternativa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-229">To specify the alternate version, set the **SecureDesktopAccommodation** key to the name of the alternate version.</span></span> <span data-ttu-id="9a03b-230">Ad esempio, se l'applicazione è stata registrata nella \_ chiave di lettura dello schermo di Contoso \_ v 1.0, è possibile registrare la versione alternativa nella schermata di Contoso \_ ReaderSecure \_ v 1.0.</span><span class="sxs-lookup"><span data-stu-id="9a03b-230">For example, if you registered your application at the Contoso\_Screen Reader\_v1.0 key, you could register the alternate version at Contoso\_Screen ReaderSecure\_v1.0.</span></span> <span data-ttu-id="9a03b-231">Impostare quindi la chiave **SecureDesktopAccommodation** di Contoso \_ Screen Reader \_ v 1.0 su "Contoso \_ Screen ReaderSecure \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="9a03b-231">Then, set the **SecureDesktopAccommodation** key of Contoso\_Screen Reader\_v1.0 to "Contoso\_Screen ReaderSecure\_v1.0".</span></span>

-   <span data-ttu-id="9a03b-232">Specificare un'applicazione Microsoft Accessibility da usare sul desktop sicuro al posto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-232">Specify a Microsoft accessibility application to use on the secure desktop in place of your application.</span></span> <span data-ttu-id="9a03b-233">Per questa opzione, impostare **SecureDesktopAccommodation** sul nome dell'applicazione di accessibilità Microsoft specifica: "OSK", "magnifierpane" o "Assistente vocale".</span><span class="sxs-lookup"><span data-stu-id="9a03b-233">For this option, set **SecureDesktopAccommodation** to the name of the particular Microsoft accessibility application: "osk", "magnifierpane", or "Narrator".</span></span>
-   <span data-ttu-id="9a03b-234">Specificare che l'applicazione non deve essere eseguita sul desktop protetto e nessuna applicazione alternativa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-234">Specify that your application should not run on the secure desktop, and neither should any alternate application.</span></span> <span data-ttu-id="9a03b-235">Per questa opzione, impostare **SecureDesktopAccommodation** su "None" (consigliato) o il nome di un'applicazione inesistente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-235">For this option, set **SecureDesktopAccommodation** to "none" (recommend) or the name of a nonexistent application.</span></span>

<span data-ttu-id="9a03b-236">Se la chiave del registro di sistema **SecureDesktopAccommodation** per l'applicazione di accessibilità specifica un'applicazione Microsoft Accessibility da eseguire sul desktop protetto al posto dell'applicazione, Windows invia una notifica all'utente quando effettua la transizione al desktop sicuro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-236">If the **SecureDesktopAccommodation** registry key for your accessibility application specifies a Microsoft accessibility application to run on the secure desktop in place of your application, Windows notifies the user of this when making the transition to the secure desktop.</span></span> <span data-ttu-id="9a03b-237">Per inviare una notifica all'utente, Windows Visualizza la stringa specificata nella chiave del registro di sistema Description per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-237">To notify the user, Windows displays the string specified in the Description registry key for your application.</span></span> <span data-ttu-id="9a03b-238">Se, ad esempio, l'applicazione ScreenReader Deluxe 1,0 utilizza l'Assistente vocale Microsoft sul desktop protetto, includerà una stringa di descrizione, ad esempio, "l'Assistente vocale Microsoft verrà usato per i desktop protetti, di accesso e di altro tipo, al posto di ScreenReader Deluxe 1,0".</span><span class="sxs-lookup"><span data-stu-id="9a03b-238">For example, if the ScreenReader Deluxe 1.0 application uses Microsoft Narrator on the secure desktop, it would include a Description string such as, "Microsoft Narrator will be used in the locked, logon, and other secure desktops in place of ScreenReader Deluxe 1.0."</span></span>

<span data-ttu-id="9a03b-239">Se la chiave **SecureDesktopAccommodation** dell'applicazione è impostata su "None", usare la chiave **Description** per indicare all'utente che l'applicazione non è disponibile sul desktop protetto e non è disponibile alcuna alternativa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-239">If your application's **SecureDesktopAccommodation** key is set to "none", use the **Description** key to tell the user your application is not available on the secure desktop and no alternative is provided.</span></span>

<span data-ttu-id="9a03b-240">Windows Visualizza il testo della descrizione nelle posizioni pertinenti nel centro di accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-240">Windows displays the Description text in the relevant locations in the Ease of Access Center.</span></span>

### <a name="running-at-installation-and-on-the-logon-desktop"></a><span data-ttu-id="9a03b-241">Esecuzione al momento dell'installazione e sul desktop di accesso</span><span class="sxs-lookup"><span data-stu-id="9a03b-241">Running at installation and on the logon desktop</span></span>

<span data-ttu-id="9a03b-242">Se si aggiunge il nome della chiave registrata dell'applicazione di accessibilità alla stringa nel seguente percorso del registro di sistema, Windows avvierà l'applicazione subito dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-242">If you append your accessibility application's registered key name to the string at the following registry location, Windows will launch your application immediately after it is installed.</span></span> <span data-ttu-id="9a03b-243">Inoltre, Windows eseguirà automaticamente l'applicazione ogni volta che il desktop di accesso è attivo.</span><span class="sxs-lookup"><span data-stu-id="9a03b-243">Also, Windows will automatically run your application whenever the logon desktop is active.</span></span>

<span data-ttu-id="9a03b-244">**\\Configurazione di \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ per HKCU Software**</span><span class="sxs-lookup"><span data-stu-id="9a03b-244">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\Configuration**</span></span>

<span data-ttu-id="9a03b-245">La chiave di configurazione è una stringa delimitata da virgole.</span><span class="sxs-lookup"><span data-stu-id="9a03b-245">The Configuration key is a comma-delimited string.</span></span> <span data-ttu-id="9a03b-246">Per aggiungere l'applicazione, aggiungere una stringa identica alla chiave del registro di sistema dell'applicazione in HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .</span><span class="sxs-lookup"><span data-stu-id="9a03b-246">To add your application, append a string that is the same as your application's registry key at HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\.</span></span>

### <a name="running-in-a-job"></a><span data-ttu-id="9a03b-247">Esecuzione in un processo</span><span class="sxs-lookup"><span data-stu-id="9a03b-247">Running in a job</span></span>

<span data-ttu-id="9a03b-248">Se la chiave del registro di sistema **TerminateOnDesktopSwitch** non è presente o è impostata su un valore diverso da zero, Windows esegue l'applicazione nel contesto di un processo, terminando e riavviando l'applicazione con ogni transizione desktop.</span><span class="sxs-lookup"><span data-stu-id="9a03b-248">If the **TerminateOnDesktopSwitch** registry key is not present or is set to non-zero, Windows runs the application in the context of a job, terminating and restarting the application with each desktop transition.</span></span> <span data-ttu-id="9a03b-249">L'esecuzione in un processo garantisce che venga eseguita una sola istanza dell'applicazione in un determinato momento e che l'applicazione non debba monitorare lo stato del desktop.</span><span class="sxs-lookup"><span data-stu-id="9a03b-249">Running in a job ensures that only a single instance of the application is running at a particular time, and frees the application from having to monitor the desktop state.</span></span> <span data-ttu-id="9a03b-250">Gli svantaggi dell'esecuzione in un processo includono:</span><span class="sxs-lookup"><span data-stu-id="9a03b-250">The disadvantages of running in a job include:</span></span>

-   <span data-ttu-id="9a03b-251">L'applicazione comporta un costo di avvio per ogni transizione del desktop.</span><span class="sxs-lookup"><span data-stu-id="9a03b-251">The application incurs a startup cost with each desktop transition.</span></span>
-   <span data-ttu-id="9a03b-252">L'applicazione può essere avviata solo tramite il Centro accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-252">The application can be started only through the Ease of Access Center.</span></span>
-   <span data-ttu-id="9a03b-253">L'applicazione deve salvare continuamente le impostazioni perché può essere terminata in qualsiasi momento da una transizione desktop.</span><span class="sxs-lookup"><span data-stu-id="9a03b-253">The application must continually save its settings because it can be terminated at any time by a desktop transition.</span></span>

<span data-ttu-id="9a03b-254">Se la chiave **TerminateOnDesktopSwitch** esiste ed è impostata su 0, Windows non esegue l'applicazione di accessibilità in un processo.</span><span class="sxs-lookup"><span data-stu-id="9a03b-254">If the **TerminateOnDesktopSwitch** key exists and is set to 0, Windows doesn't run the accessibility application in a job.</span></span> <span data-ttu-id="9a03b-255">I vantaggi di questo approccio sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a03b-255">This has the following advantages:</span></span>

-   <span data-ttu-id="9a03b-256">Nessun costo di avvio è associato a transizioni desktop.</span><span class="sxs-lookup"><span data-stu-id="9a03b-256">No startup costs are associated with desktop transitions.</span></span>
-   <span data-ttu-id="9a03b-257">L'applicazione può essere avviata al di fuori della facilità di accesso al centro.</span><span class="sxs-lookup"><span data-stu-id="9a03b-257">The application can be started outside of the Ease of Access Center.</span></span>

<span data-ttu-id="9a03b-258">Gli svantaggi di non in esecuzione in un processo includono:</span><span class="sxs-lookup"><span data-stu-id="9a03b-258">The disadvantages of not running in a job include:</span></span>

-   <span data-ttu-id="9a03b-259">Poiché l'applicazione non viene riavviata sulle transizioni desktop, deve rilevare quando il desktop corrente è inattivo e rispondere in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-259">Because the application isn t restarted on desktop transitions, it must detect when the current desktop is inactive and respond appropriately.</span></span> <span data-ttu-id="9a03b-260">Ad esempio, l'applicazione deve cedere il controllo dell'hardware, in modo che la versione desktop protetta dell'applicazione possa utilizzarla e l'applicazione deve passare alla modalità sospensione per evitare di utilizzare le risorse del processore.</span><span class="sxs-lookup"><span data-stu-id="9a03b-260">For example, the application must relinquish control of hardware so the secure desktop version of the application can use it, and the application should enter sleep mode to avoid using processor resources.</span></span>
-   <span data-ttu-id="9a03b-261">Se l'applicazione può essere avviata tramite il menu Start, Esplora risorse o la riga di comando, è necessario informare il Centro accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-261">If the application can be started through the Start menu, Windows Explorer, or the command line, the Ease of Access Center needs to be informed.</span></span> <span data-ttu-id="9a03b-262">Per ulteriori informazioni, vedere **tasto logo Windows + U**.</span><span class="sxs-lookup"><span data-stu-id="9a03b-262">For more information, see **Windows Logo key + U**.</span></span>
-   <span data-ttu-id="9a03b-263">Poiché più copie dell'applicazione possono essere eseguite contemporaneamente su diversi desktop, l'applicazione deve essere scritta per supportare più copie in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-263">Because multiple copies of the application can run simultaneously on different desktops, the application must be written to support multiple running copies.</span></span>

### <a name="windows-logo-key--u"></a><span data-ttu-id="9a03b-264">Tasto logo Windows + U</span><span class="sxs-lookup"><span data-stu-id="9a03b-264">Windows Logo key + U</span></span>

<span data-ttu-id="9a03b-265">Se l'applicazione di accessibilità è configurata per l'esecuzione in un processo, il codice di avvio dell'applicazione deve includere una chiamata alla funzione [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) per determinare se l'applicazione viene avviata in un processo.</span><span class="sxs-lookup"><span data-stu-id="9a03b-265">If your accessibility application is configured to run in a job, your application's startup code should include a call to the [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) function to determine whether the application is starting in a job.</span></span> <span data-ttu-id="9a03b-266">In tal caso, l'applicazione deve avviare il Centro accesso facilitato e quindi uscire.</span><span class="sxs-lookup"><span data-stu-id="9a03b-266">If it is, the application should start the Ease of Access Center and then exit.</span></span> <span data-ttu-id="9a03b-267">Nell'esempio seguente viene illustrato come chiamare **IsProcessInJob**.</span><span class="sxs-lookup"><span data-stu-id="9a03b-267">The following example shows how to call **IsProcessInJob**.</span></span>


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



<span data-ttu-id="9a03b-268">Se l'applicazione di accessibilità è configurata per essere eseguita all'esterno di un processo, deve notificare al centro accesso facilitato l'avvio dell'applicazione e continuare normalmente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-268">If the accessibility application is configured to run outside of a job, it should notify the Ease of Access Center that the application is starting and continue as normal.</span></span>

<span data-ttu-id="9a03b-269">Indipendentemente dal modo in cui è configurata l'applicazione, se fornisce un modo per uscire dall'applicazione, ad esempio un pulsante Chiudi, l'applicazione deve notificare al centro accessi la facilità di uscita.</span><span class="sxs-lookup"><span data-stu-id="9a03b-269">Regardless of how the application is configured, if it provides a way to exit from within the application, such as a Close button, the application must notify the Ease of Access Center that it is exiting.</span></span>

<span data-ttu-id="9a03b-270">Un'applicazione notifica la facilità di accesso al centro impostando una chiave del registro di sistema temporanea e inserendo quindi la combinazione di tasti logo Windows + U nel flusso di input.</span><span class="sxs-lookup"><span data-stu-id="9a03b-270">An application notifies the Ease of Access Center by setting a temporary registry key and then injecting the Windows Logo key + U key combination into the input stream.</span></span>

<span data-ttu-id="9a03b-271">L'applicazione deve creare la chiave temporanea nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-271">The application should create the temporary key at the following location.</span></span>

<span data-ttu-id="9a03b-272">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**</span><span class="sxs-lookup"><span data-stu-id="9a03b-272">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\AccessibilityTemp**</span></span>

<span data-ttu-id="9a03b-273">La chiave temporanea deve avere lo stesso nome del nome dell'applicazione registrata, ad esempio "Contoso \_ Screen Reader \_ v 1.0".</span><span class="sxs-lookup"><span data-stu-id="9a03b-273">The temporary key should have the same name as the registered application name, such as "Contoso\_Screen Reader\_v1.0".</span></span> <span data-ttu-id="9a03b-274">Il valore della chiave è un **DWORD** impostato su 0x0003 all'avvio oppure 0x0002 quando l'applicazione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-274">The value of the key is a **DWORD** set to 0x0003 when it is starting, or 0x0002 when the application is exiting.</span></span>


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a><span data-ttu-id="9a03b-275">Tasto logo Windows + volume su</span><span class="sxs-lookup"><span data-stu-id="9a03b-275">Windows Logo key + Volume Up</span></span>

<span data-ttu-id="9a03b-276">Quando l'utente avvia l'applicazione di accessibilità premendo la combinazione di tasti con il tasto logo Windows + volume su, ad esempio in un dispositivo tablet, il Centro accesso facilitato passa l'argomento della riga di comando seguente all'applicazione:</span><span class="sxs-lookup"><span data-stu-id="9a03b-276">When the user starts your accessibility application by pressing the Windows Logo key + Volume Up key combination (such as on a tablet device), the Ease of Access Center passes the following command-line argument to the application:</span></span>

<span data-ttu-id="9a03b-277">**/hardwarebuttonlaunch**</span><span class="sxs-lookup"><span data-stu-id="9a03b-277">**/hardwarebuttonlaunch**</span></span>

<span data-ttu-id="9a03b-278">L'applicazione può utilizzare questo argomento per determinare se avviare normalmente o per modificare di conseguenza il comportamento.</span><span class="sxs-lookup"><span data-stu-id="9a03b-278">Your application can use this argument to determine whether to start normally, or to adjust behavior accordingly.</span></span>

### <a name="transferring-secure-desktop-settings"></a><span data-ttu-id="9a03b-279">Trasferimento delle impostazioni desktop protette</span><span class="sxs-lookup"><span data-stu-id="9a03b-279">Transferring secure desktop settings</span></span>

<span data-ttu-id="9a03b-280">Se l'applicazione di accessibilità supporta il desktop protetto, è possibile usare il registro di sistema per copiare le impostazioni quando l'applicazione esegue la transizione al desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-280">If your accessibility application supports the secure desktop, you can use the registry to copy settings when the application transitions to the secure desktop.</span></span> <span data-ttu-id="9a03b-281">La copia delle impostazioni contribuisce a semplificare la transizione al desktop sicuro per l'utente.</span><span class="sxs-lookup"><span data-stu-id="9a03b-281">Copying settings helps makes the transition to the secure desktop more seamless for the user.</span></span>

<span data-ttu-id="9a03b-282">Per copiare le impostazioni, impostare la chiave del registro di sistema CopySettingsToLockedDesktop dell'applicazione su 1 e archiviare le impostazioni nel seguente percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9a03b-282">To copy settings, set the application's CopySettingsToLockedDesktop registry key to 1, and store the settings in the following registry location.</span></span>

<span data-ttu-id="9a03b-283">**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**</span><span class="sxs-lookup"><span data-stu-id="9a03b-283">**HKCU\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATConfig\\<AT Key Name>**</span></span>

<span data-ttu-id="9a03b-284">Il Centro accesso facilita il monitoraggio di questo percorso del registro di sistema mentre l'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9a03b-284">The Ease of Access Center monitors this registry location while the application is running.</span></span> <span data-ttu-id="9a03b-285">Quando si verifica una transizione al desktop protetto, la facilità di accesso al centro copia le impostazioni nello stesso percorso dell'hive HKCU del desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-285">When a transition to the secure desktop occurs, the Ease of Access Center copies the settings to the same location in the secure desktop s HKCU hive.</span></span> <span data-ttu-id="9a03b-286">L'applicazione può quindi leggere le impostazioni e riprendere il proprio stato.</span><span class="sxs-lookup"><span data-stu-id="9a03b-286">The application can then read the settings and resume its state.</span></span>

<span data-ttu-id="9a03b-287">L'applicazione di accessibilità deve scrivere le impostazioni a intervalli regolari o ogni volta che i valori cambiano.</span><span class="sxs-lookup"><span data-stu-id="9a03b-287">Your accessibility application should write its settings at regular intervals or whenever the values change.</span></span> <span data-ttu-id="9a03b-288">La scrittura delle impostazioni all'uscita dell'applicazione non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="9a03b-288">Writing settings on application exit will not work.</span></span> <span data-ttu-id="9a03b-289">Se l'applicazione è in esecuzione in un processo, viene terminata in fase di transizione dal desktop protetto, prima che sia possibile eseguire il codice di uscita.</span><span class="sxs-lookup"><span data-stu-id="9a03b-289">If the application is running in a job, it is terminated on the transition away from the secure desktop, before the exit code has a chance to run.</span></span> <span data-ttu-id="9a03b-290">Se l'applicazione non è in esecuzione in un processo, l'applicazione non viene terminata in fase di transizione dal desktop protetto.</span><span class="sxs-lookup"><span data-stu-id="9a03b-290">If the application is not running in a job, the application is not terminated on the transition away from the secure desktop.</span></span>

### <a name="caution"></a><span data-ttu-id="9a03b-291">Attenzione</span><span class="sxs-lookup"><span data-stu-id="9a03b-291">Caution</span></span>

<span data-ttu-id="9a03b-292">Poiché le chiavi del registro di sistema descritte di seguito sono scritte in modalità utente, non sono sicure.</span><span class="sxs-lookup"><span data-stu-id="9a03b-292">Because the registry keys described here are written in user mode, they are not secure.</span></span> <span data-ttu-id="9a03b-293">Se l'applicazione di accessibilità legge il contenuto di queste chiavi, deve controllare attentamente i dati e usarli con cautela.</span><span class="sxs-lookup"><span data-stu-id="9a03b-293">If your accessibility application reads the contents of these keys, it should carefully check the data and use it with caution.</span></span> <span data-ttu-id="9a03b-294">In particolare, l'applicazione deve eseguire un controllo dei limiti sui valori **DWORD** , prestare attenzione con le lunghezze di stringa, non deve leggere i nomi di DLL plug-in e non deve eseguire alcun comando trovato in stringhe.</span><span class="sxs-lookup"><span data-stu-id="9a03b-294">Specifically, your application should do a bounds check on **DWORD** values, be careful with string lengths, should not read plug-in DLL names, and should not execute any commands found in strings.</span></span>

## <a name="registry-examples"></a><span data-ttu-id="9a03b-295">Esempi di registro</span><span class="sxs-lookup"><span data-stu-id="9a03b-295">Registry Examples</span></span>

<span data-ttu-id="9a03b-296">Nell'esempio seguente vengono illustrati i possibili valori del registro di sistema per un prodotto fittizio denominato contoso ScreenReader versione 2,0, il cui nome localizzato è archiviato come risorsa.</span><span class="sxs-lookup"><span data-stu-id="9a03b-296">The following example shows the possible registry values for a fictitious product called Contoso ScreenReader version 2.0, whose localized name is stored as a resource.</span></span>

<span data-ttu-id="9a03b-297">I valori nella tabella si trovano sotto la chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="9a03b-297">The values in the table are under the following key:</span></span>

<span data-ttu-id="9a03b-298">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ Contoso \_ Screen Reader \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="9a03b-298">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Accessibility\\ATs\\Contoso\_Screen Reader\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a03b-299">Nome</span><span class="sxs-lookup"><span data-stu-id="9a03b-299">Name</span></span></th>
<th><span data-ttu-id="9a03b-300">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a03b-300">Type</span></span></th>
<th><span data-ttu-id="9a03b-301">Data</span><span class="sxs-lookup"><span data-stu-id="9a03b-301">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a03b-302">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9a03b-302">ApplicationName</span></span></td>
<td><span data-ttu-id="9a03b-303">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-303">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-304">@% SystemRoot% \system32\ContosoRes.dll,-5020</span><span class="sxs-lookup"><span data-stu-id="9a03b-304">@%SystemRoot%\system32\ContosoRes.dll,-5020</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-305">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a03b-305">Description</span></span></td>
<td><span data-ttu-id="9a03b-306">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-306">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-307">@% SystemRoot% \system32\ContosoRes.dll,-5040</span><span class="sxs-lookup"><span data-stu-id="9a03b-307">@%SystemRoot%\system32\ContosoRes.dll,-5040</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-308">Profilo</span><span class="sxs-lookup"><span data-stu-id="9a03b-308">Profile</span></span></td>
<td><span data-ttu-id="9a03b-309">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-309">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a03b-310">XML</span><span class="sxs-lookup"><span data-stu-id="9a03b-310">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-311">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="9a03b-311">SimpleProfile</span></span></td>
<td><span data-ttu-id="9a03b-312">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-312">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-313">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="9a03b-313">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-314">StartExe</span><span class="sxs-lookup"><span data-stu-id="9a03b-314">StartExe</span></span></td>
<td><span data-ttu-id="9a03b-315">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-315">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-316">C:\ContosoTools\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="9a03b-316">C:\ContosoTools\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-317">StartParams</span><span class="sxs-lookup"><span data-stu-id="9a03b-317">StartParams</span></span></td>
<td><span data-ttu-id="9a03b-318">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-318">REG_SZ</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-319">SecureDesktopAccommodation</span><span class="sxs-lookup"><span data-stu-id="9a03b-319">SecureDesktopAccommodation</span></span></td>
<td><span data-ttu-id="9a03b-320">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-320">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-321">Assistente vocale</span><span class="sxs-lookup"><span data-stu-id="9a03b-321">Narrator</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9a03b-322">Se l'applicazione fornisce sia un'applicazione per la lettura dello schermo che una lente di ingrandimento dello schermo in un singolo eseguibile, i valori per il componente Visualizzatore schermo potrebbero essere simili ai seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a03b-322">If the application provides both a screen reader and a screen magnifier in a single executable, the values for the screen reader component might look like this:</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a03b-323">Nome</span><span class="sxs-lookup"><span data-stu-id="9a03b-323">Name</span></span></th>
<th><span data-ttu-id="9a03b-324">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a03b-324">Type</span></span></th>
<th><span data-ttu-id="9a03b-325">Data</span><span class="sxs-lookup"><span data-stu-id="9a03b-325">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a03b-326">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9a03b-326">ApplicationName</span></span></td>
<td><span data-ttu-id="9a03b-327">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-327">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-328">@C:\Program Files\Contoso\Contosores.dll,-30</span><span class="sxs-lookup"><span data-stu-id="9a03b-328">@C:\Program Files\Contoso\Contosores.dll,-30</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-329">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a03b-329">Description</span></span></td>
<td><span data-ttu-id="9a03b-330">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-330">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-331">@C:\Program Files\Contoso\Contosores.dll,-32</span><span class="sxs-lookup"><span data-stu-id="9a03b-331">@C:\Program Files\Contoso\Contosores.dll,-32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-332">Profilo</span><span class="sxs-lookup"><span data-stu-id="9a03b-332">Profile</span></span></td>
<td><span data-ttu-id="9a03b-333">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-333">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a03b-334">XML</span><span class="sxs-lookup"><span data-stu-id="9a03b-334">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-335">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="9a03b-335">SimpleProfile</span></span></td>
<td><span data-ttu-id="9a03b-336">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-336">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-337">ScreenReader</span><span class="sxs-lookup"><span data-stu-id="9a03b-337">ScreenReader</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-338">StartExe</span><span class="sxs-lookup"><span data-stu-id="9a03b-338">StartExe</span></span></td>
<td><span data-ttu-id="9a03b-339">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-339">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="9a03b-340">C:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-341">StartParams</span><span class="sxs-lookup"><span data-stu-id="9a03b-341">StartParams</span></span></td>
<td><span data-ttu-id="9a03b-342">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-342">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-343">/r</span><span class="sxs-lookup"><span data-stu-id="9a03b-343">/r</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9a03b-344">I valori per il componente Magnifier si trovino nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="9a03b-344">The values for the magnifier component would be in the following key:</span></span>

<span data-ttu-id="9a03b-345">**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATS \\ Contoso \_ Magnifier \_ v 2.0**</span><span class="sxs-lookup"><span data-stu-id="9a03b-345">**HKLM\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Contosoibility\\ATs\\Contoso\_Magnifier\_v2.0**</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a03b-346">Nome</span><span class="sxs-lookup"><span data-stu-id="9a03b-346">Name</span></span></th>
<th><span data-ttu-id="9a03b-347">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a03b-347">Type</span></span></th>
<th><span data-ttu-id="9a03b-348">Data</span><span class="sxs-lookup"><span data-stu-id="9a03b-348">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a03b-349">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="9a03b-349">ApplicationName</span></span></td>
<td><span data-ttu-id="9a03b-350">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-350">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-351">@c:\Program Files\Contoso\Contosores.dll,-31</span><span class="sxs-lookup"><span data-stu-id="9a03b-351">@c:\Program Files\Contoso\Contosores.dll,-31</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-352">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a03b-352">Description</span></span></td>
<td><span data-ttu-id="9a03b-353">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-353">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-354">@c:\Program Files\Contoso\Contosores.dll,-42</span><span class="sxs-lookup"><span data-stu-id="9a03b-354">@c:\Program Files\Contoso\Contosores.dll,-42</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-355">Profilo</span><span class="sxs-lookup"><span data-stu-id="9a03b-355">Profile</span></span></td>
<td><span data-ttu-id="9a03b-356">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-356">REG_SZ</span></span></td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a03b-357">XML</span><span class="sxs-lookup"><span data-stu-id="9a03b-357">XML</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-358">SimpleProfile</span><span class="sxs-lookup"><span data-stu-id="9a03b-358">SimpleProfile</span></span></td>
<td><span data-ttu-id="9a03b-359">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-359">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-360">Ingrandimento</span><span class="sxs-lookup"><span data-stu-id="9a03b-360">Magnification</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a03b-361">StartExe</span><span class="sxs-lookup"><span data-stu-id="9a03b-361">StartExe</span></span></td>
<td><span data-ttu-id="9a03b-362">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-362">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span><span class="sxs-lookup"><span data-stu-id="9a03b-363">c:\Program Files\Contoso\Bin\ContosoSR.exe</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a03b-364">StartParams</span><span class="sxs-lookup"><span data-stu-id="9a03b-364">StartParams</span></span></td>
<td><span data-ttu-id="9a03b-365">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9a03b-365">REG_SZ</span></span></td>
<td><span data-ttu-id="9a03b-366">/m</span><span class="sxs-lookup"><span data-stu-id="9a03b-366">/m</span></span></td>
</tr>
</tbody>
</table>



 

 

