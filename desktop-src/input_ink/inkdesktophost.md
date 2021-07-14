---
description: Implementa l'interfaccia IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Classe InkDesktopHost
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689224"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="ff01d-103">Classe InkDesktopHost</span><span class="sxs-lookup"><span data-stu-id="ff01d-103">InkDesktopHost class</span></span>

<span data-ttu-id="ff01d-104">Implementa [**l'interfaccia IInkDesktopHost.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)</span><span class="sxs-lookup"><span data-stu-id="ff01d-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="ff01d-105">Un oggetto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) consente l'input penna, l'elaborazione e il rendering tramite la creazione di un thread dell'app per ospitare un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inserirlo nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.</span><span class="sxs-lookup"><span data-stu-id="ff01d-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="ff01d-106">Membri</span><span class="sxs-lookup"><span data-stu-id="ff01d-106">Members</span></span>

<span data-ttu-id="ff01d-107">La **classe InkDesktopHost** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="ff01d-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ff01d-108">**InkDesktopHost** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ff01d-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="ff01d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ff01d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ff01d-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ff01d-110">Methods</span></span>

<span data-ttu-id="ff01d-111">La **classe InkDesktopHost** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ff01d-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="ff01d-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ff01d-112">Method</span></span> | <span data-ttu-id="ff01d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff01d-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="ff01d-114">**CreateAndInitializeInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="ff01d-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="ff01d-115">Crea un [**oggetto IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in un thread dell'applicazione, lo connette alla struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app e imposta le dimensioni dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ff01d-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="ff01d-116">**CreateInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="ff01d-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="ff01d-117">Crea un [**oggetto IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) in un thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff01d-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="ff01d-118">**QueueWorkItem**</span><span class="sxs-lookup"><span data-stu-id="ff01d-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="ff01d-119">Aggiungere un'operazione di input penna a una coda di lavoro per l'esecuzione nel thread **InkDesktopHost.**</span><span class="sxs-lookup"><span data-stu-id="ff01d-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="ff01d-120">Creazione di \\ funzioni di accesso</span><span class="sxs-lookup"><span data-stu-id="ff01d-120">Creation\\Access Functions</span></span>

<span data-ttu-id="ff01d-121">Chiamare [<strong>CoCreateInstance con</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) l'identificatore di <strong>classe InkDesktopHost</strong> per recuperare un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ff01d-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="ff01d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff01d-122">Requirements</span></span>

| <span data-ttu-id="ff01d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff01d-123">Requirement</span></span> | <span data-ttu-id="ff01d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ff01d-124">Value</span></span> |
|---|---|
| <span data-ttu-id="ff01d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff01d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ff01d-126">\[Windows 10 solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ff01d-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ff01d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff01d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ff01d-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ff01d-128">None supported</span></span><br/> |
| <span data-ttu-id="ff01d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff01d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff01d-130"><dt>InkPresenterDesktop.h</dt></span><span class="sxs-lookup"><span data-stu-id="ff01d-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff01d-131">Idl</span><span class="sxs-lookup"><span data-stu-id="ff01d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff01d-132"><dt>InkPresenterDesktop.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff01d-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff01d-133">IID</span><span class="sxs-lookup"><span data-stu-id="ff01d-133">IID</span></span><br/>                      | <span data-ttu-id="ff01d-134">IID \_ IInkDesktopHost è definito come 4ce7d875-a981-4140-a1ff-ad93258e8d59</span><span class="sxs-lookup"><span data-stu-id="ff01d-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="ff01d-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff01d-135">Related topics</span></span>

<span data-ttu-id="ff01d-136">[Classi del presentatore di input](ink-presenter-classes.md)penna, interazioni con penna e [stilo,](/windows/uwp/design/input/pen-and-stylus-interactions) [esempio di](/samples/microsoft/windows-universal-samples/inkanalysis/)analisi dell'input penna, esempio di input [penna semplice,](/samples/microsoft/windows-universal-samples/simpleink/)esempio di input penna [complesso](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="ff01d-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
