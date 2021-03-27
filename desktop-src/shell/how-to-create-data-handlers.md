---
description: Estensione degli Appunti con gestori del formato dati personalizzati.
title: Come creare i gestori di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994685"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="11f4c-103">Come creare i gestori di dati</span><span class="sxs-lookup"><span data-stu-id="11f4c-103">How to Create Data Handlers</span></span>

<span data-ttu-id="11f4c-104">Quando un file viene copiato negli Appunti o trascinato e rilasciato, la shell crea un oggetto dati che supporta una varietà di [formati degli Appunti](dragdrop.md)standard.</span><span class="sxs-lookup"><span data-stu-id="11f4c-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="11f4c-105">Per i file di un tipo di file specifico, è possibile estendere i formati degli appunti disponibili implementando e registrando un *gestore di dati*.</span><span class="sxs-lookup"><span data-stu-id="11f4c-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="11f4c-106">Quando viene trasferito un file del tipo di file, la shell delega le chiamate all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati al gestore dati se viene utilizzato uno dei formati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="11f4c-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="11f4c-107">Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="11f4c-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="11f4c-108">Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di dati.</span><span class="sxs-lookup"><span data-stu-id="11f4c-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="11f4c-109">Implementazione di gestori di dati</span><span class="sxs-lookup"><span data-stu-id="11f4c-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="11f4c-110">Registrazione dei gestori di dati</span><span class="sxs-lookup"><span data-stu-id="11f4c-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="11f4c-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11f4c-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="11f4c-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="11f4c-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="11f4c-113">Passaggio 1: implementazione di gestori di dati</span><span class="sxs-lookup"><span data-stu-id="11f4c-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="11f4c-114">Come tutti i gestori di estensioni della shell, i gestori di dati sono oggetti Component Object Model in-process (COM) implementati come dll.</span><span class="sxs-lookup"><span data-stu-id="11f4c-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="11f4c-115">Esportano due interfacce, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="11f4c-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="11f4c-116">La shell Inizializza il gestore tramite la relativa interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="11f4c-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="11f4c-117">Usa questa interfaccia per richiedere l'identificatore di classe del gestore (CLSID) e fornisce il nome del file.</span><span class="sxs-lookup"><span data-stu-id="11f4c-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="11f4c-118">Per informazioni generali su come implementare i gestori di estensioni della shell, inclusa l'interfaccia **IPersistFile** , vedere [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="11f4c-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="11f4c-119">Una volta inizializzato il gestore dati, la shell delega le chiamate dall'oggetto dati all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del gestore se viene utilizzato uno dei formati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="11f4c-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="11f4c-120">Passaggio 2: registrazione dei gestori di dati</span><span class="sxs-lookup"><span data-stu-id="11f4c-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="11f4c-121">I gestori di dati sono registrati nella sottochiave *ProgID* del tipo di file, come illustrato di seguito: **HKEY \_ classi \_ radice** \\ *ProgID* \\ **ShellEx** \\ **DataHandler**</span><span class="sxs-lookup"><span data-stu-id="11f4c-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="11f4c-122">Creare una sottochiave denominata per il gestore in **DataHandler** e impostare il valore predefinito della sottochiave di tale gestore sul formato stringa del GUID CLSID del gestore.</span><span class="sxs-lookup"><span data-stu-id="11f4c-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="11f4c-123">Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="11f4c-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="11f4c-124">Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono un gestore di dati per un tipo di file con estensione MYP.</span><span class="sxs-lookup"><span data-stu-id="11f4c-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="11f4c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11f4c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f4c-126">Creazione di gestori di estensione della shell</span><span class="sxs-lookup"><span data-stu-id="11f4c-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="11f4c-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="11f4c-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="11f4c-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="11f4c-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
