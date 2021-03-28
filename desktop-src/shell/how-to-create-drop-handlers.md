---
description: Come implementare e registrare un gestore di trascinamento.
title: Come creare i gestori di rilascio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227438"
---
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="e6630-103">Come creare i gestori di rilascio</span><span class="sxs-lookup"><span data-stu-id="e6630-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="e6630-104">Per impostazione predefinita, i file non sono destinazioni di rilascio.</span><span class="sxs-lookup"><span data-stu-id="e6630-104">By default, files are not drop targets.</span></span> <span data-ttu-id="e6630-105">È possibile rendere i membri di un [tipo di file](fa-file-types.md) in drop targets implementando e registrando un *gestore di trascinamento*.</span><span class="sxs-lookup"><span data-stu-id="e6630-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="e6630-106">Se un gestore di trascinamento è registrato per un tipo di file, viene chiamato ogni volta che un oggetto viene trascinato o rilasciato in un membro del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e6630-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="e6630-107">La shell gestisce l'operazione chiamando i metodi appropriati sull'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del gestore.</span><span class="sxs-lookup"><span data-stu-id="e6630-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="e6630-108">Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e6630-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="e6630-109">Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di rilascio.</span><span class="sxs-lookup"><span data-stu-id="e6630-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="e6630-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="e6630-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="e6630-111">Passaggio 1: implementazione di gestori di rilascio</span><span class="sxs-lookup"><span data-stu-id="e6630-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="e6630-112">Come tutti i gestori di estensioni della shell, i gestori di rilascio sono oggetti COM (Component Object Model in-process) implementati come dll.</span><span class="sxs-lookup"><span data-stu-id="e6630-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="e6630-113">Esportano due interfacce, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span><span class="sxs-lookup"><span data-stu-id="e6630-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="e6630-114">La shell Inizializza il gestore tramite la relativa interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="e6630-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="e6630-115">Usa questa interfaccia per richiedere l'identificatore di classe del gestore (CLSID) e fornisce il nome del file.</span><span class="sxs-lookup"><span data-stu-id="e6630-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="e6630-116">Per informazioni generali su come implementare i gestori di estensioni della shell, inclusa l'interfaccia **IPersistFile** , vedere [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e6630-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="e6630-117">Una volta inizializzato il gestore di trascinamento, la shell chiama il metodo appropriato sull'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del gestore.</span><span class="sxs-lookup"><span data-stu-id="e6630-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="e6630-118">Passaggio 2: registrazione di gestori di rilascio</span><span class="sxs-lookup"><span data-stu-id="e6630-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="e6630-119">I gestori di rilascio sono registrati nella sottochiave di questo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="e6630-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="e6630-120">Creare una sottochiave di **DropHandler** denominata per il gestore, quindi impostare il valore predefinito della sottochiave sul formato stringa del GUID CLSID del gestore.</span><span class="sxs-lookup"><span data-stu-id="e6630-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="e6630-121">Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e6630-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="e6630-122">Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono un gestore di rilascio per un tipo di file example. MYP.</span><span class="sxs-lookup"><span data-stu-id="e6630-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="e6630-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6630-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6630-124">Creazione di gestori di estensione della shell</span><span class="sxs-lookup"><span data-stu-id="e6630-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="e6630-125">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="e6630-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="e6630-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="e6630-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
