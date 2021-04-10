---
title: Elemento THEME
description: Elemento THEME
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player Skin, elemento THEME
- Skin, elemento THEME
- Elemento THEME
- riferimento per le interfacce, elemento del tema
- elementi, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855761"
---
# <a name="theme-element"></a><span data-ttu-id="b04d7-108">Elemento THEME</span><span class="sxs-lookup"><span data-stu-id="b04d7-108">THEME Element</span></span>

<span data-ttu-id="b04d7-109">L'elemento **Theme** è l'elemento a livello padre di un'interfaccia e contiene uno o più elementi **View** , che a loro volta contengono tutti gli altri elementi all'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b04d7-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="b04d7-110">All'interno del codice di script, l'accesso all'elemento del **tema** viene effettuato tramite l'attributo globale del **tema** anziché tramite un nome specificato da un attributo **ID** , che non è supportato dall'elemento **theme** .</span><span class="sxs-lookup"><span data-stu-id="b04d7-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="b04d7-111">L'elemento **Theme** supporta gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b04d7-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="b04d7-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="b04d7-112">Attribute</span></span>                                | <span data-ttu-id="b04d7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b04d7-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b04d7-114">autore</span><span class="sxs-lookup"><span data-stu-id="b04d7-114">author</span></span>](theme-author.md)               | <span data-ttu-id="b04d7-115">Specifica o Recupera il nome dell'autore dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b04d7-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="b04d7-116">authorVersion</span><span class="sxs-lookup"><span data-stu-id="b04d7-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="b04d7-117">Specifica o Recupera il numero di versione dell'interfaccia in base a quanto assegnato dall'autore.</span><span class="sxs-lookup"><span data-stu-id="b04d7-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="b04d7-118">Copyright</span><span class="sxs-lookup"><span data-stu-id="b04d7-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="b04d7-119">Specifica o recupera la stringa del copyright per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b04d7-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="b04d7-120">currentViewID</span><span class="sxs-lookup"><span data-stu-id="b04d7-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="b04d7-121">Specifica o recupera la **visualizzazione** attualmente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="b04d7-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="b04d7-122">title</span><span class="sxs-lookup"><span data-stu-id="b04d7-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="b04d7-123">Specifica o Recupera il titolo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b04d7-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="b04d7-124">version</span><span class="sxs-lookup"><span data-stu-id="b04d7-124">version</span></span>](theme-version.md)             | <span data-ttu-id="b04d7-125">Specifica o Recupera il numero di versione di Windows Media Player per cui è stata creata l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b04d7-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="b04d7-126">Può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="b04d7-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="b04d7-127">L'elemento **Theme** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b04d7-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="b04d7-128">Metodo</span><span class="sxs-lookup"><span data-stu-id="b04d7-128">Method</span></span>                                         | <span data-ttu-id="b04d7-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b04d7-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b04d7-130">closeView</span><span class="sxs-lookup"><span data-stu-id="b04d7-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="b04d7-131">Chiude una **visualizzazione** aperta.</span><span class="sxs-lookup"><span data-stu-id="b04d7-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="b04d7-132">loadPreference</span><span class="sxs-lookup"><span data-stu-id="b04d7-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="b04d7-133">Carica una preferenza dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b04d7-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="b04d7-134">logString</span><span class="sxs-lookup"><span data-stu-id="b04d7-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="b04d7-135">Registra una stringa definita dall'utente nel file degli errori, se la registrazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b04d7-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="b04d7-136">openDialog</span><span class="sxs-lookup"><span data-stu-id="b04d7-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="b04d7-137">Apre una finestra di dialogo file.</span><span class="sxs-lookup"><span data-stu-id="b04d7-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="b04d7-138">openView</span><span class="sxs-lookup"><span data-stu-id="b04d7-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="b04d7-139">Apre una **vista** in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="b04d7-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="b04d7-140">openViewRelative</span><span class="sxs-lookup"><span data-stu-id="b04d7-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="b04d7-141">Apre una **vista** in una nuova finestra in corrispondenza della posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b04d7-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="b04d7-142">playSound</span><span class="sxs-lookup"><span data-stu-id="b04d7-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="b04d7-143">Riproduce il file audio specificato.</span><span class="sxs-lookup"><span data-stu-id="b04d7-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="b04d7-144">savePreference</span><span class="sxs-lookup"><span data-stu-id="b04d7-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="b04d7-145">Salva una preferenza nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b04d7-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="b04d7-146">showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="b04d7-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="b04d7-147">Consente di visualizzare la finestra di dialogo errore standard.</span><span class="sxs-lookup"><span data-stu-id="b04d7-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="b04d7-148">L'elemento **Theme** non supporta i gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="b04d7-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b04d7-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b04d7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b04d7-150">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="b04d7-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




