---
description: Come implementare IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Come implementare IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520498"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="1a852-103">Come implementare IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a852-103">How to Implement IUnknown</span></span>

<span data-ttu-id="1a852-104">Microsoft DirectShow si basa sul Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="1a852-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="1a852-105">Se si scrive un filtro personalizzato, è necessario implementarlo come oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="1a852-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="1a852-106">Le classi base di DirectShow forniscono un Framework dal quale eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1a852-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="1a852-107">L'uso delle classi base non è obbligatorio, ma può semplificare il processo di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="1a852-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="1a852-108">Questo articolo descrive alcuni dei dettagli interni degli oggetti COM e la relativa implementazione nelle classi base di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1a852-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="1a852-109">In questo articolo si presuppone che l'utente sia in grado di programmare le applicazioni client COM, in altre parole, di comprendere i metodi in **IUnknown**, ma non presuppone alcuna esperienza precedente nello sviluppo di oggetti com.</span><span class="sxs-lookup"><span data-stu-id="1a852-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="1a852-110">DirectShow gestisce molti dei dettagli sullo sviluppo di un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="1a852-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="1a852-111">Se si ha esperienza nello sviluppo di oggetti COM, è consigliabile leggere la sezione [uso di CUnknown](using-cunknown.md), che descrive la classe di base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="1a852-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="1a852-112">COM è una specifica, non un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="1a852-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="1a852-113">Definisce le regole che un componente deve seguire. l'inserimento di tali regole viene applicato allo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="1a852-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="1a852-114">In DirectShow tutti gli oggetti derivano da un set di classi base C++.</span><span class="sxs-lookup"><span data-stu-id="1a852-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="1a852-115">I costruttori e i metodi della classe base eseguono la maggior parte delle operazioni di "contabilità" COM, ad esempio mantenendo un conteggio dei riferimenti coerente.</span><span class="sxs-lookup"><span data-stu-id="1a852-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="1a852-116">Derivando il filtro da una classe di base, si eredita la funzionalità della classe.</span><span class="sxs-lookup"><span data-stu-id="1a852-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="1a852-117">Per utilizzare in modo efficace le classi di base, è necessario conoscere in modo generale il modo in cui implementano la specifica COM.</span><span class="sxs-lookup"><span data-stu-id="1a852-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="1a852-118">Questo articolo contiene gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a852-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="1a852-119">Funzionamento di IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a852-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="1a852-120">Uso di CUnknown</span><span class="sxs-lookup"><span data-stu-id="1a852-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="1a852-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a852-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a852-122">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="1a852-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



