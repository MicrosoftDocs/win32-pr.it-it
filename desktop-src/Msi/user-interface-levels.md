---
description: Windows Installer offre agli sviluppatori di pacchetti la possibilità di creare un'interfaccia utente interna con più livelli di funzionalità.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Livelli di interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234020"
---
# <a name="user-interface-levels"></a><span data-ttu-id="0e1ad-103">Livelli di interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0e1ad-103">User Interface Levels</span></span>

<span data-ttu-id="0e1ad-104">Windows Installer offre agli sviluppatori di pacchetti la possibilità di creare un'interfaccia utente interna con più livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="0e1ad-105">Poiché l'interfaccia utente interna deve essere creata dall'autore del pacchetto, il comportamento dell'interfaccia utente completa, l'interfaccia utente ridotta, l'interfaccia utente di base e i livelli nessuno dipendono dal pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="0e1ad-106">Nella tabella seguente vengono descritte le funzionalità comunemente attribuite ai livelli dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e1ad-107">Livello interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="0e1ad-107">UI Level</span></span></th>
<th><span data-ttu-id="0e1ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e1ad-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e1ad-109">Interfaccia utente completa</span><span class="sxs-lookup"><span data-stu-id="0e1ad-109">Full UI</span></span></td>
<td><span data-ttu-id="0e1ad-110">Consente di visualizzare le finestre di dialogo modali e non modali che sono state create nell'interfaccia utente interna.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="0e1ad-111">Visualizza le finestre di <a href="error-dialog.md">dialogo di errore</a> creati.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0e1ad-112">Le finestre di dialogo modali richiedono l'input dell'utente prima di poter continuare l'installazione e vengono specificate impostando il <a href="modal-dialog-style-bit.md">bit di stile della finestra</a> di dialogo modale nella colonna attributi della tabella della finestra di <a href="dialog-table.md">dialogo</a> .</span><span class="sxs-lookup"><span data-stu-id="0e1ad-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="0e1ad-113">Una finestra di dialogo non modale non richiede l'input dell'utente per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="0e1ad-114">Un'interfaccia utente completa comunemente presenta il <a href="user-interface-wizard-behavior.md">comportamento della procedura guidata dell'interfaccia utente</a>.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e1ad-115">Interfaccia utente ridotta</span><span class="sxs-lookup"><span data-stu-id="0e1ad-115">Reduced UI</span></span></td>
<td><span data-ttu-id="0e1ad-116">Visualizza tutte le finestre di dialogo non modali che sono state create nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="0e1ad-117">Non vengono visualizzate finestre di dialogo modali create.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="0e1ad-118">Visualizza le finestre di <a href="error-dialog.md">dialogo di errore</a> creati.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="0e1ad-119">Visualizza i messaggi di <a href="authoring-disk-prompt-messages.md">richiesta del disco</a> .</span><span class="sxs-lookup"><span data-stu-id="0e1ad-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="0e1ad-120">Visualizza le finestre di <a href="filesinuse-dialog.md">dialogo Filesinusale</a> .</span><span class="sxs-lookup"><span data-stu-id="0e1ad-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e1ad-121">Interfaccia utente di base</span><span class="sxs-lookup"><span data-stu-id="0e1ad-121">Basic UI</span></span></td>
<td><span data-ttu-id="0e1ad-122">Consente di visualizzare le finestre di dialogo non modali incorporate che mostrano i messaggi di stato.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="0e1ad-123">Consente di visualizzare le finestre di dialogo di errore predefinite.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="0e1ad-124">Non vengono visualizzate finestre di dialogo Create.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="0e1ad-125">Richiede agli utenti di inserire un disco visualizzando una finestra di dialogo contenente il valore della proprietà <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e1ad-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e1ad-126">nessuno</span><span class="sxs-lookup"><span data-stu-id="0e1ad-126">None</span></span></td>
<td><span data-ttu-id="0e1ad-127">None indica un'installazione invisibile all'utente che non visualizza alcuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0e1ad-128">Il livello dell'interfaccia utente interna può essere impostato tramite [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="0e1ad-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="0e1ad-129">Il programma di installazione imposta la proprietà [**UILevel**](uilevel.md) sul livello corrente dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="0e1ad-130">Se la proprietà [**LIMITUI**](limitui.md) è impostata, il livello di interfaccia utente utilizzato durante l'installazione del pacchetto è limitato a Basic.</span><span class="sxs-lookup"><span data-stu-id="0e1ad-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="0e1ad-131">Per un esempio di creazione dell'interfaccia utente, vedere [un esempio di installazione](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="0e1ad-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




