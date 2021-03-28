---
description: Nell'esempio seguente, una società di sviluppo software ipotetica denominata Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Esempio di associazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127867"
---
# <a name="file-association-example"></a><span data-ttu-id="112a1-103">Esempio di associazione di file</span><span class="sxs-lookup"><span data-stu-id="112a1-103">File Association Example</span></span>

<span data-ttu-id="112a1-104">Nell'esempio seguente, una società di sviluppo software ipotetica denominata Litware, Inc. crea un nuovo lettore audio denominato LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="112a1-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="112a1-105">Litware vuole progettare un'associazione di file tra LitwarePlayer e il tipo di file primario, che usa un formato audio appena sviluppato che consente l'archiviazione di un intero CD audio in meno di 10 kilobyte di memoria senza perdita di qualità.</span><span class="sxs-lookup"><span data-stu-id="112a1-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="112a1-106">Questo argomento non è applicabile a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="112a1-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="112a1-107">Il modo in cui le associazioni di file predefinite cambiano in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="112a1-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="112a1-108">Per ulteriori informazioni, vedere la sezione relativa alle **modifiche apportate al modo in cui Windows 10 gestisce le app predefinite** in [questo post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="112a1-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="112a1-109">Progettazione di una nuova associazione di file</span><span class="sxs-lookup"><span data-stu-id="112a1-109">Designing a New File Association</span></span>

<span data-ttu-id="112a1-110">La società deve eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="112a1-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="112a1-111">**Decidere se il nuovo tipo di file deve essere considerato pubblico o privato.**</span><span class="sxs-lookup"><span data-stu-id="112a1-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="112a1-112">Questo nuovo tipo di file è un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="112a1-112">This new file type is a media type.</span></span> <span data-ttu-id="112a1-113">Poiché gli utenti scambiano file multimediali su diverse piattaforme e potrebbero essere presenti altre applicazioni che devono leggere il formato LitwarePlayer, un tipo di file [pubblico](fa-file-types.md) è il più appropriato.</span><span class="sxs-lookup"><span data-stu-id="112a1-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="112a1-114">**Determinare se il tipo di file è già definito.**</span><span class="sxs-lookup"><span data-stu-id="112a1-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="112a1-115">Controllare il database MIME IANA (Internet Assigned Numbers Authority) e altri database dei tipi di file pubblici su Internet per determinare che non è stato definito alcun tipo di file analogo.</span><span class="sxs-lookup"><span data-stu-id="112a1-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="112a1-116">Poiché si tratta di un nuovo formato di file, è necessario definire un nuovo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="112a1-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="112a1-117">**Definire un'estensione del nome file per il nuovo tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="112a1-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="112a1-118">Gli sviluppatori scelgono `.opa-ltw-audio` , che incorpora l'abbreviazione del fornitore e un suggerimento sul contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="112a1-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="112a1-119">La ricerca determina che l'estensione non è usata da altri utenti.</span><span class="sxs-lookup"><span data-stu-id="112a1-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="112a1-120">Seguendo le raccomandazioni correnti, non viene definita alcuna estensione breve.</span><span class="sxs-lookup"><span data-stu-id="112a1-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="112a1-121">**Definire un tipo MIME per il tipo di file e registrarlo con IANA.**</span><span class="sxs-lookup"><span data-stu-id="112a1-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="112a1-122">Litware definisce il nuovo tipo MIME come *audio/LitwarePlayer. 1* e prepara un'applicazione di tipo MIME, seguendo le linee guida previste nei numeri RFC (Request for Comments) 2045, 2046, 2047 e 2048.</span><span class="sxs-lookup"><span data-stu-id="112a1-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="112a1-123">Quindi inviano l'applicazione a IANA, che aggiunge il nuovo tipo di file al database dei tipi MIME registrati.</span><span class="sxs-lookup"><span data-stu-id="112a1-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="112a1-124">**Determinare se esiste un ProgID per il tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="112a1-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="112a1-125">Poiché si tratta di un nuovo tipo di file, non esiste alcun [ProgID](fa-progids.md) .</span><span class="sxs-lookup"><span data-stu-id="112a1-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="112a1-126">Litware imposta sulla progettazione di un nuovo ProgID per LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="112a1-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="112a1-127">Decidono il nome descrittivo "LitwarePlayer Audio Player" (archiviato come risorsa nel file LitwarePlayer.exe) e progettano un'icona predefinita da usare per i file associati a LitwarePlayer (archiviati anche in LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="112a1-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="112a1-128">Poiché LitwarePlayer è una nuova applicazione, si tratta di un ProgID della versione 1.</span><span class="sxs-lookup"><span data-stu-id="112a1-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="112a1-129">**Registrare il ProgID.**</span><span class="sxs-lookup"><span data-stu-id="112a1-129">**Register the ProgID.**</span></span> <span data-ttu-id="112a1-130">Quando LitwarePlayer è installato, il programma di installazione crea la voce [ProgID](fa-progids.md) seguente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="112a1-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

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

    <span data-ttu-id="112a1-131">Nella chiave del comando %1 viene passato come percorso del file da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="112a1-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="112a1-132">**Registrare l'estensione del nome file per il tipo di file.**</span><span class="sxs-lookup"><span data-stu-id="112a1-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="112a1-133">Quando LitwarePlayer è installato, il programma di installazione crea le seguenti voci nel registro di sistema per l'estensione del tipo di file personalizzato.</span><span class="sxs-lookup"><span data-stu-id="112a1-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="112a1-134">Ogni volta che viene creata o modificata un'associazione di file, notificare al sistema che è stata apportata una modifica chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specificando l' \_ evento SHCNE ASSOCCHANGED.</span><span class="sxs-lookup"><span data-stu-id="112a1-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="112a1-135">Se questa operazione non viene eseguita, è possibile che la shell non riconosca le modifiche apportate fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="112a1-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="112a1-136">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="112a1-136">Additional Resources</span></span>

-   [<span data-ttu-id="112a1-137">Introduzione alle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="112a1-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="112a1-138">Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows</span><span class="sxs-lookup"><span data-stu-id="112a1-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="112a1-139">[Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="112a1-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="112a1-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="112a1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="112a1-141">Procedure consigliate per le associazioni di file</span><span class="sxs-lookup"><span data-stu-id="112a1-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="112a1-142">Linee guida per la gestione di applicazioni predefinite in Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="112a1-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="112a1-143">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="112a1-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="112a1-144">Impostazione dell'accesso al programma e delle impostazioni predefinite del computer (SPAD)</span><span class="sxs-lookup"><span data-stu-id="112a1-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
