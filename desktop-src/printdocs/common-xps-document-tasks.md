---
description: In questa pagina sono elencate alcune delle attività di programmazione comunemente eseguite con l'API del documento XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Attività comuni di programmazione di documenti XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311830"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="d9a5b-103">Attività comuni di programmazione di documenti XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="d9a5b-104">In questa pagina sono elencate alcune delle attività di programmazione comunemente eseguite con l'API del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="d9a5b-105">Attività comuni relative ai documenti XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="d9a5b-106">Negli esempi di codice seguenti vengono illustrate alcune delle attività di programmazione che vengono in genere eseguite quando l'API del documento XPS viene utilizzata per l'utilizzo di un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="d9a5b-107">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="d9a5b-108">Creazione di un OM XPS vuoto</span><span class="sxs-lookup"><span data-stu-id="d9a5b-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="d9a5b-109">Leggere un documento XPS in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="d9a5b-110">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="d9a5b-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="d9a5b-111">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="d9a5b-112">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="d9a5b-113">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="d9a5b-114">Scrivere un OM XPS in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="d9a5b-115">Stampare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="d9a5b-116">Uso delle interfacce di raccolta OM XPS</span><span class="sxs-lookup"><span data-stu-id="d9a5b-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="d9a5b-117">Dichiarazione di non responsabilità</span><span class="sxs-lookup"><span data-stu-id="d9a5b-117">Disclaimer</span></span>

<span data-ttu-id="d9a5b-118">Gli esempi di codice non sono destinati a essere programmi completi e funzionanti.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="d9a5b-119">Gli esempi di codice a cui si fa riferimento in questa pagina, ad esempio, non eseguono il controllo dei parametri, il controllo degli errori o la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="d9a5b-120">Usare questi esempi come punto di partenza e quindi aggiungere il codice necessario per creare un'applicazione affidabile.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="d9a5b-121">Per ulteriori informazioni sui valori restituiti **HRESULT** e sulle strategie di gestione degli errori, vedere [gestione degli errori in com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="d9a5b-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="d9a5b-122">Prima di poter utilizzare le interfacce XPS OM, è necessario inizializzare COM nel thread, come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="d9a5b-123">Per maggiore chiarezza, questi esempi di codice usano un OM XPS molto semplice, uno che potrebbe non essere sufficientemente complesso per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="d9a5b-124">Come esempio, negli esempi di codice che aggiungono contenuto a una pagina gli elementi visivi di una pagina vengono aggiunti direttamente all'elenco di oggetti visivi della pagina; in pratica, tuttavia, è possibile raggruppare gli oggetti visivi in oggetti Canvas, in modo che sia possibile agire su più oggetti come un gruppo.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="d9a5b-125">Pertanto, per abilitare il supporto dello stesso contenuto per più di una dimensione di pagina, è possibile raggruppare il contenuto visivo di una pagina in un singolo oggetto Canvas, quindi applicare una trasformazione all'area di disegno per adattarla alle dimensioni correnti della pagina.</span><span class="sxs-lookup"><span data-stu-id="d9a5b-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9a5b-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9a5b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9a5b-127">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="d9a5b-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="d9a5b-128">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="d9a5b-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
