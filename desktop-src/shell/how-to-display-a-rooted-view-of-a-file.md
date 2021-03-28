---
description: È possibile utilizzare un'estensione dello spazio dei nomi per consentire agli utenti di esplorare il contenuto di un file anziché presentarlo come cartella. Le estensioni di questo tipo vengono in genere utilizzate per visualizzare il contenuto dei membri di un tipo di file.
title: Come visualizzare una visualizzazione radice di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881573"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="47bfa-104">Come visualizzare una visualizzazione radice di un file</span><span class="sxs-lookup"><span data-stu-id="47bfa-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="47bfa-105">È possibile utilizzare un'estensione dello spazio dei nomi per consentire agli utenti di esplorare il contenuto di un file anziché presentarlo come cartella.</span><span class="sxs-lookup"><span data-stu-id="47bfa-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="47bfa-106">Le estensioni di questo tipo vengono in genere utilizzate per visualizzare il contenuto dei membri di un [tipo di file](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="47bfa-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="47bfa-107">Ad esempio, i membri di un tipo di file potrebbero contenere più file o immagini compresse, organizzati in una gerarchia.</span><span class="sxs-lookup"><span data-stu-id="47bfa-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="47bfa-108">Invece di scrivere un'applicazione per consentire all'utente di visualizzare il contenuto di un file di questo tipo, è possibile scrivere un'estensione dello spazio dei nomi e lasciare che Esplora risorse gestisca la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="47bfa-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="47bfa-109">Per fare in modo che un'estensione visualizzi il contenuto di un file, è necessario utilizzare una vista radice.</span><span class="sxs-lookup"><span data-stu-id="47bfa-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="47bfa-110">Il modo più comune per fornire una visualizzazione radice dei membri di un tipo di file consiste nel definire un [verbo di menu di scelta rapida](context.md) che avvii un'istanza di Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="47bfa-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="47bfa-111">Se si imposta questo verbo come verbo predefinito, un doppio clic apre anche una visualizzazione radice del file.</span><span class="sxs-lookup"><span data-stu-id="47bfa-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="47bfa-112">È possibile definire un verbo per tutti i membri del tipo di file [modificando il registro di sistema](context.md)o definire in modo dinamico i verbi in base al file mediante l'implementazione di un [gestore di menu di scelta rapida](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="47bfa-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="47bfa-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="47bfa-113">Instructions</span></span>


<span data-ttu-id="47bfa-114">Nell'esempio seguente viene illustrato come utilizzare il registro di sistema per fornire una visualizzazione radice dei membri di un tipo di file modificando il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="47bfa-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="47bfa-115">La voce del registro di sistema di esempio è una modifica di uno degli esempi nell' [estensione dei menu di scelta rapida](context.md).</span><span class="sxs-lookup"><span data-stu-id="47bfa-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="47bfa-116">Le voci del registro di sistema definiscono i file con estensione MYP come tipo di file e usano il verbo **Browse** per avviare una visualizzazione radice dei membri di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="47bfa-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

<span data-ttu-id="47bfa-117">È possibile usare lo stesso verbo per avviare a livello di codice una visualizzazione radice di un membro del tipo di file chiamando la funzione [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="47bfa-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47bfa-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47bfa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47bfa-119">Impostazione della posizione di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47bfa-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="47bfa-120">Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="47bfa-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="47bfa-121">Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento</span><span class="sxs-lookup"><span data-stu-id="47bfa-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="47bfa-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="47bfa-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



