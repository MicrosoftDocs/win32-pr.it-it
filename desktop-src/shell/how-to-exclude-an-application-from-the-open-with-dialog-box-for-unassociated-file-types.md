---
description: Come escludere un'applicazione dalla finestra di dialogo Apri con per il tipo di file non associato.
title: Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563322"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a><span data-ttu-id="70183-103">Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati</span><span class="sxs-lookup"><span data-stu-id="70183-103">How to Exclude an Application from the Open With Dialog Box for Unassociated File Types</span></span>

<span data-ttu-id="70183-104">Quando un utente tenta di aprire un file che non è un membro di un tipo di file registrato, ovvero un tipo di file sconosciuto, oppure quando un utente seleziona **Apri con** o **apri con-> scegliere programma predefinito** dal menu di scelta rapida di un file, la shell Visualizza un sottomenu o una finestra di dialogo che consente all'utente di specificare il programma utilizzato per aprire il file.</span><span class="sxs-lookup"><span data-stu-id="70183-104">When a user attempts to open a file that is not a member of any registered file type (that is, an unknown file type), or when a user selects **Open with** or **Open with -> Choose default program** from a file's shortcut menu, the Shell presents a submenu or dialog box that enables the user to specify the program used to open the file.</span></span>

<span data-ttu-id="70183-105">Per impostazione predefinita, qualsiasi applicazione registrata come sottochiave delle applicazioni **\_ \_ radice delle classi HKEY** \\  viene visualizzata nella finestra di dialogo **Apri con** .</span><span class="sxs-lookup"><span data-stu-id="70183-105">By default, any application registered as a subkey of **HKEY\_CLASSES\_ROOT**\\**Applications** is presented in the **Open with** dialog box.</span></span> <span data-ttu-id="70183-106">Queste applicazioni vengono presentate in modo **aperto** , indipendentemente dal fatto che l'applicazione sia registrata per gestire il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="70183-106">These applications are presented in **Open with** regardless of whether the application is registered to handle the file type.</span></span>

<span data-ttu-id="70183-107">Per impedire che un'applicazione venga visualizzata nella finestra di dialogo **Apri con** quando l'applicazione non deve o non può essere utilizzata per aprire determinati tipi di file, utilizzare una delle due tecniche descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="70183-107">To prevent an application from appearing in the **Open with** dialog box when the application should not or cannot be used to open certain file types, use one of the two techniques described in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="70183-108">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="70183-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="70183-109">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="70183-109">Step 1:</span></span>

<span data-ttu-id="70183-110">Aggiungere una voce NoOpenWith alla sottochiave dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="70183-110">Add a NoOpenWith entry to the application's subkey.</span></span> <span data-ttu-id="70183-111">Quando un'applicazione utilizza un tipo di file, Windows registra tali informazioni per compilare l'elenco dei **Programmi consigliati** .</span><span class="sxs-lookup"><span data-stu-id="70183-111">When an application uses a file type, Windows records that information to build the **Recommended Programs** list.</span></span> <span data-ttu-id="70183-112">Questo elenco viene visualizzato nel sottomenu **Apri con** , come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="70183-112">This list is presented in the **Open with** submenu as shown in the following screen shot.</span></span>

![screenshot del menu di scelta rapida con il sottomenu Apri con visualizzato](images/file-assoc/openwithsubmenu.png)

<span data-ttu-id="70183-114">Queste applicazioni consigliate sono inoltre visualizzate nella parte **Programmi consigliati** della finestra di dialogo **Apri con** , come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="70183-114">These recommended applications are also shown in the **Recommended Programs** portion of the **Open with** dialog box as shown in the following screen shot.</span></span>

![screenshot della finestra di dialogo Apri con con i programmi consigliati](images/file-assoc/openwithdialog.png)

> [!Note]  
> <span data-ttu-id="70183-116">Se un'applicazione è stata registrata in [OpenWithList](fa-file-types.md) o OpenWithProgIDs per il tipo di file, verrà visualizzata nell'elenco **Programmi consigliati** anche se è impostata la voce NoOpenWith.</span><span class="sxs-lookup"><span data-stu-id="70183-116">If an application has registered itself in the [OpenWithList](fa-file-types.md) or OpenWithProgIDs for the file type, it will appear in the **Recommended Programs** list even if the NoOpenWith entry is set.</span></span> <span data-ttu-id="70183-117">Tenere inoltre presente che, indipendentemente dal fatto che un'applicazione venga offerta in un elenco di programmi consigliati, un utente può passare manualmente a qualsiasi file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="70183-117">Also, remember that regardless of whether an application is offered in a list of recommended programs, a user can manually browse to any executable file.</span></span>

 

<span data-ttu-id="70183-118">Le applicazioni possono disabilitare questo rilevamento specificando un valore NoOpenWith nella sottochiave dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="70183-118">Applications can disable this tracking by specifying a NoOpenWith value under the application's subkey.</span></span>

<span data-ttu-id="70183-119">La voce NoOpenWith è un valore **reg \_ SZ** vuoto, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="70183-119">The NoOpenWith entry is an empty **REG\_SZ** value as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

<span data-ttu-id="70183-120">L'impostazione della voce NoOpenWith presenta anche questi effetti:</span><span class="sxs-lookup"><span data-stu-id="70183-120">Setting the NoOpenWith entry also has these effects:</span></span>

-   <span data-ttu-id="70183-121">Impedisce l'aggiunta di un file alla Jump List dell'applicazione tramite il trascinamento della selezione, a meno che l'applicazione non sia stata registrata in modo specifico per gestire il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="70183-121">Prevents pinning a file to the application's Jump List through drag-and-drop, unless the application is specifically registered to handle that file type.</span></span>
-   <span data-ttu-id="70183-122">Impedisce alla finestra di dialogo file comune e a qualsiasi chiamata alla funzione [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) di aggiungere qualsiasi file alla Jump List dell'applicazione, a meno che l'applicazione non sia stata registrata in modo specifico per gestire il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="70183-122">Prevents the common file dialog box and any call to the [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) function from adding any file to the application's Jump List, unless the application is specifically registered to handle that file type.</span></span>

### <a name="step-2"></a><span data-ttu-id="70183-123">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="70183-123">Step 2:</span></span>

<span data-ttu-id="70183-124">Il secondo modo per impedire che un'applicazione venga visualizzata nella finestra di dialogo **Apri con** , consiste nell'usare la sottochiave **SupportedTypes** per elencare in modo esplicito le estensioni dei tipi di file che l'applicazione può aprire.</span><span class="sxs-lookup"><span data-stu-id="70183-124">The second way to prevent an application from appearing in the **Open with** dialog box is to use the **SupportedTypes** subkey to explicitly list the extensions of file types that the application can open.</span></span> <span data-ttu-id="70183-125">In questo modo si impedisce che l'applicazione venga visualizzata nella finestra di dialogo **Apri con** per i tipi di file che non è in grado di aprire.</span><span class="sxs-lookup"><span data-stu-id="70183-125">This prevents the application from appearing in the **Open with** dialog box for file types that it cannot open.</span></span> <span data-ttu-id="70183-126">Fa anche in modo che l'applicazione venga visualizzata nell'elenco **Programmi consigliati** , come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="70183-126">It also causes the application to appear in the **Recommended Programs** list as discussed previously.</span></span>

<span data-ttu-id="70183-127">Questo metodo è particolarmente utile se un'applicazione può salvare un file come un determinato tipo di file ma non è in grado di aprire il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="70183-127">This method is particularly useful if an application can save a file as a certain file type but cannot open that file type.</span></span> <span data-ttu-id="70183-128">Un'applicazione deve inoltre impostare il \_ flag Fos DONTADDTORECENT tramite [**IFileDialog:: SetOption**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) quando si chiama la finestra di dialogo **Salva** .</span><span class="sxs-lookup"><span data-stu-id="70183-128">An application should also set the FOS\_DONTADDTORECENT flag through [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) when calling the **Save** dialog box.</span></span> <span data-ttu-id="70183-129">In questo modo si impedisce l'aggiunta dell'elemento alle parti **recenti** o **frequenti** di una Jump List.</span><span class="sxs-lookup"><span data-stu-id="70183-129">This keeps the item from being added to the **Recent** or **Frequent** portions of a Jump List.</span></span> <span data-ttu-id="70183-130">Impedisce inoltre di tenere traccia dell'applicazione in [OpenWithList](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="70183-130">It also blocks the application from being tracked under [OpenWithList](fa-file-types.md).</span></span>

<span data-ttu-id="70183-131">Ogni estensione supportata viene aggiunta come voce sotto la sottochiave **SupportedTypes** , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="70183-131">Each supported extension is added as an entry under the **SupportedTypes** subkey as shown in the following example.</span></span> <span data-ttu-id="70183-132">Le voci sono di tipo **reg \_ SZ** o **reg \_ null**, senza valori associati.</span><span class="sxs-lookup"><span data-stu-id="70183-132">The entries are of type **REG\_SZ** or **REG\_NULL**, with no associated values.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

<span data-ttu-id="70183-133">Se viene fornita una sottochiave **SupportedTypes** , solo i file con tali estensioni sono idonei per l'aggiunta alla Jump List dell'applicazione o per essere rilevati nell'elenco di destinazioni **recenti** o **frequenti** di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="70183-133">If a **SupportedTypes** subkey is provided, only files with those extensions are eligible for pinning to the application's Jump List or for being tracked in an application's **Recent** or **Frequent** destinations list.</span></span>

<span data-ttu-id="70183-134">La voce NoOpenWith esegue l'override della sottochiave **SupportedTypes** e nasconde l'applicazione nella finestra di dialogo **Apri con** .</span><span class="sxs-lookup"><span data-stu-id="70183-134">The NoOpenWith entry overrides the **SupportedTypes** subkey and hides the application in the **Open with** dialog box.</span></span>

 

 
