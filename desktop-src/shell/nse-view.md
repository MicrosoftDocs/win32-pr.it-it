---
description: La maggior parte delle estensioni dello spazio dei nomi è un subset dello spazio dei nomi shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980007"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="e71cd-103">Visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e71cd-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="e71cd-104">La maggior parte delle estensioni dello spazio dei nomi è un subset dello spazio dei nomi shell.</span><span class="sxs-lookup"><span data-stu-id="e71cd-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="e71cd-105">Quando si crea un punto di giunzione, come descritto in [specifica della posizione di un'estensione dello spazio dei nomi](nse-junction.md), Esplora risorse consente agli utenti di spostarsi all'interno e all'esterno dell'estensione dello spazio dei nomi come qualsiasi altra cartella.</span><span class="sxs-lookup"><span data-stu-id="e71cd-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="e71cd-106">Tuttavia, è anche possibile usare Esplora risorse per visualizzare solo il contenuto dell'estensione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e71cd-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="e71cd-107">Questa opzione di visualizzazione viene a volte definita *visualizzazione radice*.</span><span class="sxs-lookup"><span data-stu-id="e71cd-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="e71cd-108">Sebbene non sia comunemente utilizzato, le visualizzazioni radice possono essere preferibili alle visualizzazioni normali per alcuni tipi di estensioni.</span><span class="sxs-lookup"><span data-stu-id="e71cd-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="e71cd-109">Con una visualizzazione con radice, viene creata una nuova istanza di Esplora risorse che Visualizza il contenuto dell'estensione come spazio dei nomi separato.</span><span class="sxs-lookup"><span data-stu-id="e71cd-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="e71cd-110">La visualizzazione struttura ad albero di una visualizzazione radice Mostra solo le cartelle che fanno parte dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e71cd-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="e71cd-111">Gli utenti non possono spostarsi da una vista radice ad altre parti dello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="e71cd-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="e71cd-112">Le estensioni vengono implementate nello stesso modo per le visualizzazioni con radice così come sono per le visualizzazioni normali.</span><span class="sxs-lookup"><span data-stu-id="e71cd-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="e71cd-113">L'unica differenza è rappresentata dal modo in cui il contenuto dell'estensione viene visualizzato da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e71cd-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="e71cd-114">È anche possibile avere viste normali e con radice della stessa estensione.</span><span class="sxs-lookup"><span data-stu-id="e71cd-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="e71cd-115">Per aprire una vista di un'estensione, è necessario avviare un'istanza di Explorer.exe con un flag/root.</span><span class="sxs-lookup"><span data-stu-id="e71cd-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="e71cd-116">Esistono diversi modi per avviare una visualizzazione con radice, a seconda della natura dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e71cd-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="e71cd-117">Come usare un punto di giunzione per aprire una visualizzazione con radice</span><span class="sxs-lookup"><span data-stu-id="e71cd-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="e71cd-118">Come usare un file di collegamento per aprire una visualizzazione con radice</span><span class="sxs-lookup"><span data-stu-id="e71cd-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="e71cd-119">Come visualizzare una visualizzazione radice di un file</span><span class="sxs-lookup"><span data-stu-id="e71cd-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 



