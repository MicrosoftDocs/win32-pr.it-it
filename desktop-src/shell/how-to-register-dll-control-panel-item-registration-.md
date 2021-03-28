---
description: Gli elementi del pannello di controllo implementati in una DLL che esporta la funzione CPlApplet presentano requisiti di registrazione diversi rispetto ai file exe.
title: Come registrare gli elementi del pannello di controllo DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756506"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="f21df-103">Come registrare gli elementi del pannello di controllo DLL</span><span class="sxs-lookup"><span data-stu-id="f21df-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="f21df-104">Le linee guida di implementazione correnti affermano che i nuovi elementi del pannello di controllo devono essere implementati come file con estensione exe anziché come file con estensione CPL.</span><span class="sxs-lookup"><span data-stu-id="f21df-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="f21df-105">Le informazioni seguenti sono incluse principalmente per finalità legacy.</span><span class="sxs-lookup"><span data-stu-id="f21df-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="f21df-106">Gli elementi del pannello di controllo implementati in una DLL che esporta la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) presentano requisiti di registrazione diversi rispetto ai file exe.</span><span class="sxs-lookup"><span data-stu-id="f21df-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="f21df-107">A partire da Windows XP, è necessario installare nuove dll elemento del pannello di controllo nella cartella dell'applicazione associata nella cartella programmi.</span><span class="sxs-lookup"><span data-stu-id="f21df-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="f21df-108">Gli elementi archiviati nella directory system32 con estensione CPL non devono essere registrati. vengono visualizzati automaticamente nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="f21df-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="f21df-109">Tutti gli altri elementi del pannello di controllo che usano **CPlApplet** devono essere registrati in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f21df-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="f21df-110">Se l'elemento del pannello di controllo deve essere disponibile per tutti gli utenti, registrare il percorso in base al computer aggiungendo un valore **reg \_ expand \_ SZ** alla sottochiave CPLS del computer **\_ locale \_ HKEY** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Control Panel** \\  , impostata sul percorso della dll.</span><span class="sxs-lookup"><span data-stu-id="f21df-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="f21df-111">Se l'elemento del pannello di controllo deve essere disponibile per ogni utente, usare **HKEY \_ Current \_ User** come chiave radice anziché **HKEY \_ Local \_ computer**.</span><span class="sxs-lookup"><span data-stu-id="f21df-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="f21df-112">Nei due esempi seguenti viene registrato l'elemento del pannello di controllo *MyCplApp* .</span><span class="sxs-lookup"><span data-stu-id="f21df-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="f21df-113">Il nome della DLL è MyCpl.cpl e si *trova nella directory dell' \\ applicazione MyApplication* .</span><span class="sxs-lookup"><span data-stu-id="f21df-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="f21df-114">Nel primo esempio viene illustrata la registrazione per computer.</span><span class="sxs-lookup"><span data-stu-id="f21df-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="f21df-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f21df-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f21df-116">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="f21df-116">Step 1:</span></span>

<span data-ttu-id="f21df-117">Aggiungere queste informazioni al registro di sistema per registrare l'esistenza del file con estensione CPL.</span><span class="sxs-lookup"><span data-stu-id="f21df-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="f21df-118">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="f21df-118">Step 2:</span></span>

<span data-ttu-id="f21df-119">**Windows Vista e versioni successive:** Aggiungere queste informazioni aggiuntive al registro di sistema per fornire un GUID per l'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="f21df-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="f21df-120">Generando un GUID per identificare in modo univoco l'elemento del pannello di controllo, è possibile aggiungere collegamenti alle attività nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="f21df-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="f21df-121">Senza questo GUID, non esiste alcun modo per associare i collegamenti dell'attività all'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="f21df-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="f21df-122">[Per un elemento del pannello di controllo, vedere Creazione di collegamenti alle attività ricercabili](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="f21df-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="f21df-123">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="f21df-123">Step 3:</span></span>

<span data-ttu-id="f21df-124">**Windows Vista e versioni successive:** Aggiungere al registro di sistema le informazioni seguenti per creare un nome canonico per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="f21df-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="f21df-125">Aggiungendo un nome canonico, gli utenti possono avviare l'elemento del pannello di controllo da una riga di comando immettendo `control.exe /name MyCorporation.MyCpl` .</span><span class="sxs-lookup"><span data-stu-id="f21df-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="f21df-126">In questo modo è possibile anche modificare un'implementazione da un file con estensione CPL in un file con estensione exe in un secondo momento, senza che sia necessario chiamare programmi per apportare modifiche, in quanto possono continuare ad aprire l'elemento tramite il nome canonico.</span><span class="sxs-lookup"><span data-stu-id="f21df-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="f21df-127">Per ulteriori informazioni sui nomi canonici, vedere [esecuzione di elementi del pannello di controllo](executing-control-panel-items.md).</span><span class="sxs-lookup"><span data-stu-id="f21df-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="f21df-128">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="f21df-128">Step 4:</span></span>

<span data-ttu-id="f21df-129">**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al registro di sistema per assegnare un elemento del pannello di controllo a una o più categorie.</span><span class="sxs-lookup"><span data-stu-id="f21df-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="f21df-130">**Windows XP:** Aggiungere le informazioni seguenti al registro di sistema per assegnare un elemento del pannello di controllo a una o più categorie.</span><span class="sxs-lookup"><span data-stu-id="f21df-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="f21df-131">In questo esempio l'elemento viene assegnato alla categoria 3, ovvero rete e Internet.</span><span class="sxs-lookup"><span data-stu-id="f21df-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="f21df-132">Per aggiungere un elemento a più categorie, fornire l'elenco come valore REG \_ SZ separato da virgole, ad esempio "3, 8".</span><span class="sxs-lookup"><span data-stu-id="f21df-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="f21df-133">I valori possono essere specificati in formato decimale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="f21df-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="f21df-134">Si noti che la possibilità di aggiungere un elemento a più categorie è possibile solo in Windows XP Service Pack 2 (SP2) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f21df-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="f21df-135">Vedere [assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md) per tutti i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="f21df-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="f21df-136">Passaggio 5:</span><span class="sxs-lookup"><span data-stu-id="f21df-136">Step 5:</span></span>

<span data-ttu-id="f21df-137">**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al registro di sistema per creare e puntare a un file XML per archiviare i collegamenti alle attività per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="f21df-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="f21df-138">Il valore deve essere un \_ percorso reg SZ, come illustrato qui, o un modulo e un ID di risorsa (ad esempio, "C: \\ Program Files \\ Corp \\ MyApp \\MyApp.exe,-31") se si tratta di una risorsa incorporata.</span><span class="sxs-lookup"><span data-stu-id="f21df-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="f21df-139">Il percorso del file XML deve essere specificato in modo completo.</span><span class="sxs-lookup"><span data-stu-id="f21df-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="f21df-140">Non può usare una variabile di ambiente, ad esempio% ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="f21df-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="f21df-141">Per altri dettagli sui collegamenti alle attività e su come creare il file XML in cui tenerli, vedere [creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="f21df-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f21df-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f21df-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f21df-143">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="f21df-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="f21df-144">Come registrare gli elementi del pannello di controllo eseguibile</span><span class="sxs-lookup"><span data-stu-id="f21df-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
