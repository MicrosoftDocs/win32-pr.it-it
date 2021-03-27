---
description: In questa sezione viene illustrata la creazione di menu di scelta rapida (contesto) e l'implementazione di gestori di menu di scelta rapida.
title: Menu di scelta rapida (contesto) e gestori di menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225931"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="ce1aa-103">Menu di scelta rapida (contesto) e gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="ce1aa-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="ce1aa-104">In questa sezione viene illustrata la creazione di menu di scelta rapida (contesto) e l'implementazione di gestori di menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="ce1aa-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="ce1aa-105">Questa sezione relativa ai tipi di file e alle associazioni di file è organizzata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ce1aa-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="ce1aa-106">Verbi e associazioni di file</span><span class="sxs-lookup"><span data-stu-id="ce1aa-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="ce1aa-107">Scelta di un metodo di menu di scelta rapida statico o dinamico</span><span class="sxs-lookup"><span data-stu-id="ce1aa-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="ce1aa-108">Procedure consigliate per i gestori di menu di scelta rapida e più verbi</span><span class="sxs-lookup"><span data-stu-id="ce1aa-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="ce1aa-109">Creazione di gestori di menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="ce1aa-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="ce1aa-110">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="ce1aa-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="ce1aa-111">Come escludere e controllare la visibilità del verbo</span><span class="sxs-lookup"><span data-stu-id="ce1aa-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="ce1aa-112">Come utilizzare il modello di selezione dei verbi</span><span class="sxs-lookup"><span data-stu-id="ce1aa-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="ce1aa-113">Come usare gli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="ce1aa-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="ce1aa-114">Come implementare verbi personalizzati per le cartelle tramite Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="ce1aa-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="ce1aa-115">Personalizzazione di un menu di scelta rapida tramite verbi dinamici</span><span class="sxs-lookup"><span data-stu-id="ce1aa-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="ce1aa-116">Come implementare l'interfaccia IContextMenu</span><span class="sxs-lookup"><span data-stu-id="ce1aa-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="ce1aa-117">Riferimento al menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="ce1aa-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="ce1aa-118">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="ce1aa-118">Additional Resources</span></span>

<span data-ttu-id="ce1aa-119">Per informazioni di base concettuali correlate, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce1aa-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="ce1aa-120">[Introduzione alle associazioni di file](fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="ce1aa-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="ce1aa-121">Per estendere la shell con i gestori di tipi di file, vedere [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ce1aa-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="ce1aa-122">Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="ce1aa-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="ce1aa-123">Per informazioni di riferimento correlate documentazione, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce1aa-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="ce1aa-124">Per eseguire un verbo su un elemento della shell, vedere il metodo [**InvokeVerb**](folderitem-invokeverb.md) .</span><span class="sxs-lookup"><span data-stu-id="ce1aa-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="ce1aa-125">Per recuperare una raccolta di verbi che possono essere eseguiti su un elemento della shell, vedere il metodo [**verbs**](folderitem-verbs.md) .</span><span class="sxs-lookup"><span data-stu-id="ce1aa-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="ce1aa-126">Per eseguire un'operazione su un file specificato, vedere le funzioni [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="ce1aa-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



