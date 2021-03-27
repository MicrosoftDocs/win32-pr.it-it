---
description: In questo argomento viene illustrato come registrare un gestore di anteprime associato a un determinato tipo di dati.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Come registrare un gestore di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979519"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="a6b72-103">Come registrare un gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="a6b72-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="a6b72-104">In questo argomento viene illustrato come registrare un gestore di anteprime associato a un determinato tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="a6b72-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="a6b72-105">Ai fini dell'illustrazione, gli esempi in questo argomento usano un tipo di file xyz.</span><span class="sxs-lookup"><span data-stu-id="a6b72-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="a6b72-106">La registrazione di un gestore di anteprime è una registrazione standard basata sull'associazione di file.</span><span class="sxs-lookup"><span data-stu-id="a6b72-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="a6b72-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="a6b72-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a6b72-108">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="a6b72-108">Step 1:</span></span>

<span data-ttu-id="a6b72-109">Per prima cosa, un'estensione del nome file è associata a un ProgID.</span><span class="sxs-lookup"><span data-stu-id="a6b72-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="a6b72-110">La voce seguente associa la sottochiave ProgID **xyzfile** con l'estensione del nome di file xyz.</span><span class="sxs-lookup"><span data-stu-id="a6b72-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="a6b72-111">La sottochiave ProgID **xyzfile** viene archiviata con gli altri ProgID, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a6b72-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="a6b72-112">Ogni sottochiave ProgID del gestore di anteprime contiene una sottochiave denominata **ShellEx** che contiene una sottochiave denominata *sempre* **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span><span class="sxs-lookup"><span data-stu-id="a6b72-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="a6b72-113">La presenza della sottochiave indica al sistema che il gestore è un gestore di anteprime.</span><span class="sxs-lookup"><span data-stu-id="a6b72-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="a6b72-114">Il valore predefinito della sottochiave **{8895b1c6-b41f-4c1c-a562-0d564250836f}** è l'identificatore di classe (CLSID) del gestore.</span><span class="sxs-lookup"><span data-stu-id="a6b72-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="a6b72-115">Di seguito è riportato un esempio della sottochiave ProgID **xyzfile** , che associa un gestore di CLSID {ec3a629a-a47c-4245-BC78-b4b63d0e3154}.</span><span class="sxs-lookup"><span data-stu-id="a6b72-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="a6b72-116">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="a6b72-116">Step 2:</span></span>

<span data-ttu-id="a6b72-117">Successivamente, aggiungere la sottochiave in **CLSID** per il gestore di anteprime.</span><span class="sxs-lookup"><span data-stu-id="a6b72-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="a6b72-118">Un esempio è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a6b72-118">An example is shown here.</span></span> <span data-ttu-id="a6b72-119">Segue una spiegazione delle singole voci.</span><span class="sxs-lookup"><span data-stu-id="a6b72-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="a6b72-120">Il valore predefinito per la sottochiave (in questo caso, **{ec3a629a-a47c-4245-BC78-b4b63d0e3154}**) non è obbligatorio o utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a6b72-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="a6b72-121">Tuttavia, l'impostazione su una stringa non localizzata può consentire di eseguire il debug dei problemi di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a6b72-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="a6b72-122">Il segno meno (-101) nella risorsa. dll nella voce DisplayName esiste per motivi legacy.</span><span class="sxs-lookup"><span data-stu-id="a6b72-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="a6b72-123">La voce dell'icona, d'altra parte, non richiede un segno meno.</span><span class="sxs-lookup"><span data-stu-id="a6b72-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="a6b72-124">Il valore AppID fornisce un riferimento all'AppID dell'applicazione associata all'estensione del nome file, archiviata in **HKEY \_ classi \_ radice** \\ **AppID**.</span><span class="sxs-lookup"><span data-stu-id="a6b72-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="a6b72-125">Il valore usato qui, {6d2b5079-2f0b-48DD-ab7f-97cec514d30b}, è l'ID dell'host surrogato Prevhost.exe.</span><span class="sxs-lookup"><span data-stu-id="a6b72-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="a6b72-126">i gestori di anteprime a 32 bit devono usare **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando vengono installati nei sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a6b72-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="a6b72-127">Le voci sotto la sottochiave **InprocServer32** includono un riferimento alla sottochiave ProgID dell'estensione del nome file e una voce per [VersionIndependentProgID](../com/versionindependentprogid.md).</span><span class="sxs-lookup"><span data-stu-id="a6b72-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="a6b72-128">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="a6b72-128">Step 3:</span></span>

<span data-ttu-id="a6b72-129">Infine, il gestore di anteprime deve essere aggiunto all'elenco di tutti i gestori di anteprime.</span><span class="sxs-lookup"><span data-stu-id="a6b72-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="a6b72-130">Questo elenco viene usato come ottimizzazione dal sistema per enumerare tutti i gestori di anteprime registrati a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a6b72-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="a6b72-131">Anche in questo caso, il valore predefinito non è obbligatorio, ma semplicemente il processo di debug.</span><span class="sxs-lookup"><span data-stu-id="a6b72-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="a6b72-132">In Windows 7, se l'applicazione è installata per tutti gli utenti del computer, utilizzare HKEY \_ Local \_ computer; se per un solo utente, utilizzare HKEY \_ Current \_ User.</span><span class="sxs-lookup"><span data-stu-id="a6b72-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="a6b72-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6b72-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b72-134">Gestori di anteprime e host di anteprima della shell</span><span class="sxs-lookup"><span data-stu-id="a6b72-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="a6b72-135">Compilazione di gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="a6b72-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="a6b72-136">Linee guida per il gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="a6b72-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
