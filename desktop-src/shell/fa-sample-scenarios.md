---
description: Nell'esempio seguente, un'ipotetica società di sviluppo software denominata Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Esempio di associazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b92922bb907c4dd90b3e2bdc3d16c8e8b52e6a
ms.sourcegitcommit: b0d03febac36ff77cba034615b94ea103311398d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/19/2021
ms.locfileid: "107715789"
---
# <a name="file-association-example"></a><span data-ttu-id="3bd7e-103">Esempio di associazione di file</span><span class="sxs-lookup"><span data-stu-id="3bd7e-103">File Association Example</span></span>

<span data-ttu-id="3bd7e-104">Nell'esempio seguente, un'ipotetica società di sviluppo software denominata Litware, Inc. crea un nuovo lettore audio denominato LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="3bd7e-105">Litware vuole progettare un'associazione di file tra LitwarePlayer e il relativo tipo di file primario, che usa un formato audio appena sviluppato che consente di archiviare un intero CD audio in meno di 10 kilobyte di memoria senza perdita di qualità.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bd7e-106">Questo argomento non si applica a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="3bd7e-107">Il funzionamento delle associazioni di file predefinite è stato modificato in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="3bd7e-108">Per altre informazioni, vedere la sezione Modifiche **alla modalità Windows 10 le app predefinite** in questo [post.](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)</span><span class="sxs-lookup"><span data-stu-id="3bd7e-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="3bd7e-109">Progettazione di una nuova associazione di file</span><span class="sxs-lookup"><span data-stu-id="3bd7e-109">Designing a New File Association</span></span>

<span data-ttu-id="3bd7e-110">L'azienda deve eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="3bd7e-111">**Decidere se il nuovo tipo di file deve essere considerato pubblico o privato.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="3bd7e-112">Questo nuovo tipo di file è un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-112">This new file type is a media type.</span></span> <span data-ttu-id="3bd7e-113">Poiché gli utenti scambiano file multimediali tra diverse piattaforme e potrebbero essere presenti altre applicazioni che devono leggere il formato LitwarePlayer, un tipo [di](fa-file-types.md) file pubblico è il più appropriato.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="3bd7e-114">**Determinare se questo tipo di file è già definito.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="3bd7e-115">Controllare il database MIME IANA (Internet Assigned Numbers Authority) e altri database di tipi di file pubblici su Internet per determinare che non è stato definito alcun tipo di file confrontabile.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="3bd7e-116">Poiché si tratta di un nuovo formato di file, è necessario definire un nuovo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="3bd7e-117">**Definire un'estensione di file per il nuovo tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="3bd7e-118">Gli sviluppatori scelgono , che incorpora l'abbreviazione del fornitore e un `.opa-ltw-audio` suggerimento sul contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="3bd7e-119">La ricerca determina che l'estensione non viene usata da altri utenti.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="3bd7e-120">In base alle raccomandazioni correnti, non viene definita alcuna estensione breve.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="3bd7e-121">**Definire un tipo MIME per il tipo di file e registrarlo con IANA.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="3bd7e-122">Litware definisce il nuovo tipo MIME come *audio/LitwarePlayer.1* e prepara un'applicazione di tipo MIME, seguendo le linee guida illustrate nei numeri RFC 2045, 2046, 2047 e 2048.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="3bd7e-123">Inviano quindi l'applicazione all'IANA, che aggiunge il nuovo tipo di file al database di tipi MIME registrati.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="3bd7e-124">**Determinare se esiste un ProgID per il tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="3bd7e-125">Poiché si tratta di un nuovo tipo di file, non esiste [alcun ProgID.](fa-progids.md)</span><span class="sxs-lookup"><span data-stu-id="3bd7e-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="3bd7e-126">Litware imposta sulla progettazione di un nuovo ProgID per LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="3bd7e-127">Decidono il nome descrittivo "LitwarePlayer Audio Player" (archiviato come risorsa nel file LitwarePlayer.exe) e progettano un'icona predefinita da usare per i file associati a LitwarePlayer (archiviati anche in LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="3bd7e-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="3bd7e-128">Poiché LitwarePlayer è una nuova applicazione, si tratta di un ProgID versione 1.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="3bd7e-129">**Registrare progID.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-129">**Register the ProgID.**</span></span> <span data-ttu-id="3bd7e-130">Quando LitwarePlayer è installato, il programma di installazione crea la voce [ProgID](fa-progids.md) seguente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="3bd7e-131">Nella chiave di comando % 1 viene passato come percorso del file da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="3bd7e-132">**Registrare l'estensione del nome file per il tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="3bd7e-133">Quando LitwarePlayer è installato, il programma di installazione crea le voci seguenti nel Registro di sistema per l'estensione del tipo di file personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="3bd7e-134">Ogni volta che viene creata o modificata un'associazione di file, notificare al sistema che è stata apportata una modifica chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l'evento SHCNE \_ ASSOCCHANGED.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="3bd7e-135">Se questa operazione non viene eseguita, shell potrebbe non riconoscere le modifiche apportate fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="3bd7e-136">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3bd7e-136">Additional Resources</span></span>

-   [<span data-ttu-id="3bd7e-137">Introduzione alle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="3bd7e-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="3bd7e-138">Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows</span><span class="sxs-lookup"><span data-stu-id="3bd7e-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="3bd7e-139">[Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3bd7e-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bd7e-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bd7e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bd7e-141">Procedure consigliate per le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="3bd7e-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="3bd7e-142">Linee guida per la gestione delle applicazioni predefinite in Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="3bd7e-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="3bd7e-143">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="3bd7e-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="3bd7e-144">Impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)</span><span class="sxs-lookup"><span data-stu-id="3bd7e-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
