---
title: Controlli Rich Edit senza finestra
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con controlli Rich Edit senza finestra.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044318"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="ac79f-103">Controlli Rich Edit senza finestra</span><span class="sxs-lookup"><span data-stu-id="ac79f-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="ac79f-104">Questa sezione contiene informazioni sugli elementi di programmazione usati con controlli Rich Edit senza finestra.</span><span class="sxs-lookup"><span data-stu-id="ac79f-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="ac79f-105">Il Component Object Model (COM) definisce un set di interfacce per supportare gli oggetti privi di finestra.</span><span class="sxs-lookup"><span data-stu-id="ac79f-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="ac79f-106">Gli oggetti senza finestra possono entrare nello stato attivo sul posto senza avere la propria finestra, ma usare invece la finestra del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ac79f-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="ac79f-107">Di conseguenza, un oggetto senza finestra utilizza un minor numero di risorse di sistema e offre prestazioni migliori grazie all'attivazione e alla disattivazione più veloci.</span><span class="sxs-lookup"><span data-stu-id="ac79f-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="ac79f-108">Gli oggetti senza finestra, inoltre, possono essere non rettangolari e trasparenti.</span><span class="sxs-lookup"><span data-stu-id="ac79f-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="ac79f-109">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="ac79f-109">Overviews</span></span>



| <span data-ttu-id="ac79f-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="ac79f-110">Topic</span></span>                                                                          | <span data-ttu-id="ac79f-111">Contenuto</span><span class="sxs-lookup"><span data-stu-id="ac79f-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac79f-112">Informazioni sui controlli Rich Edit senza finestra</span><span class="sxs-lookup"><span data-stu-id="ac79f-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="ac79f-113">Un controllo Rich Edit senza finestra, noto anche come oggetto servizi di testo, è un oggetto che fornisce la funzionalità di un [controllo Rich Edit](rich-edit-controls.md) senza fornire la finestra.</span><span class="sxs-lookup"><span data-stu-id="ac79f-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="ac79f-114">Funzioni</span><span class="sxs-lookup"><span data-stu-id="ac79f-114">Functions</span></span>



| <span data-ttu-id="ac79f-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="ac79f-115">Topic</span></span>                                            | <span data-ttu-id="ac79f-116">Contenuto</span><span class="sxs-lookup"><span data-stu-id="ac79f-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac79f-117">**CreateTextServices**</span><span class="sxs-lookup"><span data-stu-id="ac79f-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="ac79f-118">La funzione [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crea un'istanza di un oggetto servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="ac79f-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="ac79f-119">L'oggetto servizi di testo supporta varie interfacce, tra cui [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e il modello a oggetti di testo (Tom).</span><span class="sxs-lookup"><span data-stu-id="ac79f-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="ac79f-120">Interfacce</span><span class="sxs-lookup"><span data-stu-id="ac79f-120">Interfaces</span></span>



| <span data-ttu-id="ac79f-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="ac79f-121">Topic</span></span>                                  | <span data-ttu-id="ac79f-122">Contenuto</span><span class="sxs-lookup"><span data-stu-id="ac79f-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac79f-123">**ITextHost**</span><span class="sxs-lookup"><span data-stu-id="ac79f-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="ac79f-124">L'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) viene utilizzata da un oggetto servizi di testo per ottenere i servizi host di testo.</span><span class="sxs-lookup"><span data-stu-id="ac79f-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="ac79f-125">**ITextServices**</span><span class="sxs-lookup"><span data-stu-id="ac79f-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="ac79f-126">Estende il TOM per fornire funzionalità aggiuntive per l'operazione senza finestra.</span><span class="sxs-lookup"><span data-stu-id="ac79f-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





