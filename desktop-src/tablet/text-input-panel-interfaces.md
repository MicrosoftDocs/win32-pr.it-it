---
description: In questa sezione vengono fornite informazioni sulle interfacce utilizzate per controllare l'aspetto e il comportamento del pannello input penna di Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfacce del pannello di input di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233856"
---
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="e5a1a-103">Interfacce del pannello di input di testo</span><span class="sxs-lookup"><span data-stu-id="e5a1a-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="e5a1a-104">In questa sezione vengono fornite informazioni sulle interfacce utilizzate per controllare l'aspetto e il comportamento del pannello input penna di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="e5a1a-105">Le interfacce del pannello di input di testo non sono conformi all'automazione.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e5a1a-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e5a1a-106">In This Section</span></span>



| <span data-ttu-id="e5a1a-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e5a1a-107">Interface</span></span>                                                                | <span data-ttu-id="e5a1a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5a1a-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5a1a-109">**Interfaccia IHandWrittenTextInsertion**</span><span class="sxs-lookup"><span data-stu-id="e5a1a-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="e5a1a-110">Usato dal codice di immissione di testo personalizzato dell'applicazione per inserire il testo nel campo di testo e nell'archivio di backup dei servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="e5a1a-111">**Interfaccia ITextInputPanel**</span><span class="sxs-lookup"><span data-stu-id="e5a1a-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="e5a1a-112">Fornisce il controllo sul pannello input penna di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e5a1a-113">**Interfaccia ITextInputPanelEventSink**</span><span class="sxs-lookup"><span data-stu-id="e5a1a-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="e5a1a-114">Definisce i metodi che gestiscono gli eventi dell' [**interfaccia ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .</span><span class="sxs-lookup"><span data-stu-id="e5a1a-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="e5a1a-115">**Interfaccia ITextInputPanelRunInfo**</span><span class="sxs-lookup"><span data-stu-id="e5a1a-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="e5a1a-116">Fornisce un metodo per determinare se il pannello di input di testo è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="e5a1a-117">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="e5a1a-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="e5a1a-118">Consente al client di chiamare l'oggetto provider di completamento automatico del pannello di input di testo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="e5a1a-119">**Interfaccia ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="e5a1a-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="e5a1a-120">Gestisce il lato dell'applicazione dell'integrazione di completamento automatico del pannello di input di testo.</span><span class="sxs-lookup"><span data-stu-id="e5a1a-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="e5a1a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5a1a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a1a-122">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="e5a1a-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




