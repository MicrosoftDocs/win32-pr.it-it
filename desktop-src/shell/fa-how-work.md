---
description: Le associazioni di file definiscono il modo in cui la shell considera un tipo di file nel sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Funzionamento delle associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227455"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="a07a5-103">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-103">How File Associations Work</span></span>

<span data-ttu-id="a07a5-104">Le associazioni di file definiscono il modo in cui la shell considera un [tipo di file](fa-file-types.md) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a07a5-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="a07a5-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a07a5-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a07a5-106">Informazioni sulle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="a07a5-107">Quando è necessario implementare o modificare le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="a07a5-108">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="a07a5-109">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a07a5-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a07a5-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a07a5-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="a07a5-111">Informazioni sulle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-111">About File Associations</span></span>

<span data-ttu-id="a07a5-112">Le associazioni di file controllano le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="a07a5-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="a07a5-113">Quale applicazione viene avviata quando un utente fa doppio clic su un file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="a07a5-114">Quale icona appare per un file per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a07a5-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="a07a5-115">Visualizzazione del tipo di file visualizzato in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="a07a5-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="a07a5-116">Comandi visualizzati nel menu di scelta rapida di un file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="a07a5-117">Altre funzionalità dell'interfaccia utente, ad esempio le descrizioni comandi, le informazioni sui riquadri e il riquadro dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="a07a5-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="a07a5-118">Gli sviluppatori di applicazioni possono utilizzare le associazioni di file per controllare il modo in cui la shell considera i tipi di file personalizzati o per associare un'applicazione ai tipi di file esistenti.</span><span class="sxs-lookup"><span data-stu-id="a07a5-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="a07a5-119">Ad esempio, quando un'applicazione viene installata, l'applicazione può verificare la presenza di associazioni di file esistenti e creare o eseguire l'override di tali associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="a07a5-120">Gli utenti possono controllare alcuni aspetti delle associazioni di file per personalizzare il modo in cui la shell considera un tipo di file usando l'interfaccia utente **aperta con** oppure modificando il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a07a5-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="a07a5-121">Nella finestra di Esplora risorse visualizzata nella schermata seguente la shell Visualizza icone diverse per ogni file, in base all'icona associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="a07a5-122">Se l'utente fa doppio clic sull' **immagine bitmap di esempio** file, la shell avvia Paint e la usa per aprire il file perché in questo sistema, Paint è associato ai file con estensione bmp.</span><span class="sxs-lookup"><span data-stu-id="a07a5-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="a07a5-123">Gli utenti possono controllare queste azioni usando le associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-123">People can control these actions using file associations.</span></span>

![illustrazione di come funzionano le associazioni di file in pratica](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="a07a5-125">Quando è necessario implementare o modificare le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="a07a5-126">Le applicazioni possono utilizzare i file per diversi scopi: alcuni file vengono utilizzati esclusivamente dall'applicazione e non sono in genere accessibili dagli utenti, mentre gli altri file vengono creati dall'utente e spesso vengono aperti, cercati e visualizzati dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="a07a5-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="a07a5-127">A meno che il tipo di file personalizzato non venga usato esclusivamente dall'applicazione, è necessario implementare le associazioni di file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="a07a5-128">Come regola generale, implementare le associazioni di file per il tipo di file personalizzato se si prevede che l'utente interagisca direttamente con questi file in qualsiasi modo.</span><span class="sxs-lookup"><span data-stu-id="a07a5-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="a07a5-129">Che include l'uso della Shell per esplorare e aprire i file, cercare il contenuto o le proprietà dei file e visualizzare in anteprima i file.</span><span class="sxs-lookup"><span data-stu-id="a07a5-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="a07a5-130">Se l'applicazione gestisce un tipo di file esistente, non modificare l'associazione file, a meno che non si desideri modificare il modo in cui la shell gestisce tutti i file di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="a07a5-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="a07a5-131">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-131">How File Associations Work</span></span>

<span data-ttu-id="a07a5-132">I file vengono esposti nella shell come elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="a07a5-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="a07a5-133">Per controllare le associazioni di file, gli sviluppatori di applicazioni possono registrare un mapping tra il tipo di file e i gestori (oggetti COM che forniscono funzionalità per gli elementi della shell del tipo di file).</span><span class="sxs-lookup"><span data-stu-id="a07a5-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="a07a5-134">Quando la shell deve eseguire una query per le associazioni di file di un tipo di file, crea una matrice di chiavi del registro di sistema contenenti le associazioni per il tipo di file e controlla queste chiavi per le associazioni di file appropriate da usare.</span><span class="sxs-lookup"><span data-stu-id="a07a5-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a07a5-135">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a07a5-135">Additional Resources</span></span>

-   <span data-ttu-id="a07a5-136">Per informazioni di base concettuali sulle associazioni di file, vedere [Cenni preliminari su verbi e associazioni di file](fa-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="a07a5-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a07a5-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a07a5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a07a5-138">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="a07a5-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="a07a5-139">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="a07a5-140">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="a07a5-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="a07a5-141">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="a07a5-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="a07a5-142">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="a07a5-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="a07a5-143">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="a07a5-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="a07a5-144">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="a07a5-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="a07a5-145">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="a07a5-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



