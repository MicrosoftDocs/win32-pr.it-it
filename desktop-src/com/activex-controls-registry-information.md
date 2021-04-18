---
title: Informazioni del registro di sistema controlli ActiveX
description: Informazioni del registro di sistema controlli ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517139"
---
# <a name="activex-controls-registry-information"></a><span data-ttu-id="992d1-103">Informazioni del registro di sistema controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="992d1-103">ActiveX Controls Registry Information</span></span>

<span data-ttu-id="992d1-104">Sono disponibili diverse voci del registro di sistema e flag utilizzati.</span><span class="sxs-lookup"><span data-stu-id="992d1-104">There are a number of registry entries and flags that are used.</span></span> <span data-ttu-id="992d1-105">Inoltre, i controlli possono supportare le categorie di componenti per classificare le funzionalità che forniscono.</span><span class="sxs-lookup"><span data-stu-id="992d1-105">Additionally, controls can support component categories to classify the features they provide.</span></span>

<span data-ttu-id="992d1-106">Le chiavi del registro di sistema correlate ai controlli sono contrassegnate con un asterisco nell'albero seguente:</span><span class="sxs-lookup"><span data-stu-id="992d1-106">Registry keys related to controls are marked with an asterisk in the following tree:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

<span data-ttu-id="992d1-107">La voce **DefaultIcon** viene utilizzata per identificare un'icona da visualizzare quando il controllo è ridotto a icona.</span><span class="sxs-lookup"><span data-stu-id="992d1-107">The **DefaultIcon** entry is used to identify an icon to be displayed when the control is minimized to an icon.</span></span> <span data-ttu-id="992d1-108">La funzione [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) viene usata per ottenere l'icona da. DLL o. File EXE specificato.</span><span class="sxs-lookup"><span data-stu-id="992d1-108">The [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) function is used to get the icon from the .DLL or .EXE file specified.</span></span>

<span data-ttu-id="992d1-109">La voce **ToolboxBitmap32** identifica il nome del modulo e l'identificatore di risorsa per una \* bitmap di 16 15 da usare per la superficie di una barra degli strumenti o un pulsante della casella degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="992d1-109">The **ToolboxBitmap32** entry identifies the module name and resource identifier for a 16\*15 bitmap to use for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="992d1-110">Le dimensioni dell'icona standard di Windows sono troppo grandi per essere usate a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="992d1-110">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="992d1-111">Questa voce supporta in modo specifico i contenitori di controllo che dispongono di una modalità di progettazione in cui uno seleziona i controlli e li inserisce in un modulo progettato.</span><span class="sxs-lookup"><span data-stu-id="992d1-111">This entry specifically supports control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span> <span data-ttu-id="992d1-112">In Visual Basic, ad esempio, l'icona del controllo viene visualizzata nella casella degli strumenti Visual Basic durante la modalità progettazione.</span><span class="sxs-lookup"><span data-stu-id="992d1-112">For example, in Visual Basic, the control's icon is displayed in the Visual Basic toolbox during design mode.</span></span>

<span data-ttu-id="992d1-113">La voce di **controllo** contrassegna un oggetto come controllo.</span><span class="sxs-lookup"><span data-stu-id="992d1-113">The **Control** entry marks an object as a control.</span></span> <span data-ttu-id="992d1-114">Questa voce viene spesso usata dai contenitori per compilare le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="992d1-114">This entry is often used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="992d1-115">Il contenitore usa questa sottochiave per determinare se includere un oggetto in una finestra di dialogo in cui sono visualizzati i controlli.</span><span class="sxs-lookup"><span data-stu-id="992d1-115">The container uses this sub-key to determine whether to include an object in a dialog box that displays controls.</span></span>

<span data-ttu-id="992d1-116">La chiave secondaria **inseribile** può essere usata anche con i controlli, a seconda che l'oggetto possa agire solo come oggetto incorporato sul posto senza funzionalità di controllo speciali.</span><span class="sxs-lookup"><span data-stu-id="992d1-116">The **Insertable** sub-key can also be used with controls, depending on whether the object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="992d1-117">Gli oggetti contrassegnati con **Insertable** vengono visualizzati nella finestra di dialogo Inserisci oggetto del relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="992d1-117">Objects marked with **Insertable** appear in the Insert Object dialog box of their container.</span></span> <span data-ttu-id="992d1-118">La voce **Insertable** indica in genere che il controllo è stato testato con contenitori non di controllo.</span><span class="sxs-lookup"><span data-stu-id="992d1-118">The **Insertable** entry generally means that the control has been tested with non-control containers.</span></span>

<span data-ttu-id="992d1-119">I sottochiavi **Insertable** e **Control** sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="992d1-119">Both the **Insertable** and the **Control** sub-keys are optional.</span></span> <span data-ttu-id="992d1-120">Un controllo può omettere la sottochiave **inseribile** se non è progettata per funzionare con i contenitori meno recenti che non comprendono i controlli.</span><span class="sxs-lookup"><span data-stu-id="992d1-120">A control can omit the **Insertable** sub-key if it not designed to work with older containers that do not understand controls.</span></span> <span data-ttu-id="992d1-121">Un controllo può omettere la chiave del **controllo** se è progettata solo per funzionare con un contenitore specifico e pertanto non vuole essere inserita in altri contenitori.</span><span class="sxs-lookup"><span data-stu-id="992d1-121">A control can omit the **Control** key if it is only designed to work with a specific container and thus does not wish to be inserted in other containers.</span></span>

<span data-ttu-id="992d1-122">I controlli devono avere un verbo Properties, \_ le proprietà OLEIVERB, insieme a tutti gli altri verbi supportati.</span><span class="sxs-lookup"><span data-stu-id="992d1-122">Controls should have a Properties verb, OLEIVERB\_PROPERTIES, along with any other verbs they support.</span></span> <span data-ttu-id="992d1-123">Il verbo Properties, così come il verbo standard OLEIVERB \_ Primary, indica al controllo di visualizzare la relativa finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="992d1-123">The Properties verb, as well as the standard verb OLEIVERB\_PRIMARY, instructs the control to display its property sheet.</span></span> <span data-ttu-id="992d1-124">Il verbo Properties viene visualizzato come elemento Properties nel menu del contenitore quando il controllo è attivo.</span><span class="sxs-lookup"><span data-stu-id="992d1-124">The Properties verb is displayed as the Properties item on the container's menu when the control is active.</span></span> <span data-ttu-id="992d1-125">In questo modo, il controllo può visualizzare la propria pagina delle proprietà che consente alcune funzionalità utili all'utente finale, anche se il contenitore non gestisce i controlli.</span><span class="sxs-lookup"><span data-stu-id="992d1-125">This way, the control can display its own property page allowing some useful functionality to the end user, even if the container does not handle controls.</span></span>

<span data-ttu-id="992d1-126">Un controllo definisce la chiave **miscStatus** per la descrizione di contenitori potenziali.</span><span class="sxs-lookup"><span data-stu-id="992d1-126">A control defines the **MiscStatus** key to describe itself to potential containers.</span></span> <span data-ttu-id="992d1-127">I bit accettano i valori di [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)e i controlli aggiungono diversi valori a questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="992d1-127">The bits take on the values from [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), and controls add several values to this enumeration.</span></span> <span data-ttu-id="992d1-128">Per ulteriori informazioni, vedere i valori di enumerazione **OLEMISC** .</span><span class="sxs-lookup"><span data-stu-id="992d1-128">See the **OLEMISC** enumeration values for more information.</span></span> <span data-ttu-id="992d1-129">Il client può ottenere queste informazioni chiamando [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) senza dover creare prima un'istanza del controllo.</span><span class="sxs-lookup"><span data-stu-id="992d1-129">The client can obtain this information by calling [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) without having to instantiate the control first.</span></span>

<span data-ttu-id="992d1-130">Infine, **Version** descrive la versione del controllo che deve corrispondere alla versione della libreria dei tipi associata a questo controllo.</span><span class="sxs-lookup"><span data-stu-id="992d1-130">Finally, **Version** describes the version of the control which should match the version of the type library associated with this control.</span></span>

<span data-ttu-id="992d1-131">Inoltre, nelle informazioni sul tipo per un controllo, il controllo attributo contrassegna una voce della coclasse come descrizione di un controllo.</span><span class="sxs-lookup"><span data-stu-id="992d1-131">Also in the type information for a control, the attribute control marks a coclass entry as describing a control.</span></span>

 

 