---
title: Classi ausiliarie dinamiche
description: Analogamente alle classi di oggetti strutturali e astratte, le classi ausiliarie sono definite da un oggetto classSchema nello schema Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Active Directory (classi ausiliarie dinamiche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472579"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="63f38-104">Classi ausiliarie dinamiche</span><span class="sxs-lookup"><span data-stu-id="63f38-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="63f38-105">Analogamente alle classi di oggetti strutturali e astratte, le classi ausiliarie sono definite da un oggetto [**classSchema**](/windows/desktop/ADSchema/c-classschema) nello schema Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63f38-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="63f38-106">Per altre informazioni, vedere [classi strutturali, astratte e ausiliarie](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="63f38-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="63f38-107">Questa definizione dello schema specifica varie caratteristiche della classe, inclusi gli attributi associati alla classe.</span><span class="sxs-lookup"><span data-stu-id="63f38-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="63f38-108">Diversamente dalle classi strutturali, non è possibile creare un'istanza di una classe ausiliaria come si può con una classe strutturale.</span><span class="sxs-lookup"><span data-stu-id="63f38-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="63f38-109">Usare invece una classe ausiliaria per estendere l'elenco di attributi associato a un'altra classe di oggetti strutturale, astratta o ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="63f38-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="63f38-110">Nella versione iniziale di Windows 2000 Active Directory Domain Services fornito supporto per collegare staticamente le classi ausiliarie alla definizione [**classSchema**](/windows/desktop/ADSchema/c-classschema) di un'altra classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="63f38-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="63f38-111">Quando una classe ausiliaria viene utilizzata in questo modo, ogni istanza della classe di oggetti supporta gli attributi della classe ausiliaria.</span><span class="sxs-lookup"><span data-stu-id="63f38-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="63f38-112">**Windows 2000 Server e versioni precedenti:** Active Directory Domain Services non fornisce supporto per collegare in modo dinamico le classi ausiliarie a singoli oggetti e non solo a intere classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="63f38-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="63f38-113">Inoltre, le classi ausiliarie associate a un'istanza di oggetto non possono essere successivamente rimosse dall'istanza di.</span><span class="sxs-lookup"><span data-stu-id="63f38-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="63f38-114">**Windows Server 2003:** Le classi ausiliarie dinamiche sono supportate quando tutti i controller di dominio della foresta eseguono Windows Server 2003 e la modalità funzionale della foresta è Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="63f38-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="63f38-115">Per ulteriori informazioni sulle classi ausiliarie, vedere:</span><span class="sxs-lookup"><span data-stu-id="63f38-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="63f38-116">Classi ausiliarie collegate in modo dinamico</span><span class="sxs-lookup"><span data-stu-id="63f38-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="63f38-117">Classi ausiliarie collegate in modo statico</span><span class="sxs-lookup"><span data-stu-id="63f38-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="63f38-118">Determinazione delle classi associate a un'istanza dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="63f38-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="63f38-119">Aggiunta di una classe ausiliaria a un'istanza di oggetto</span><span class="sxs-lookup"><span data-stu-id="63f38-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="63f38-120">Per ulteriori informazioni sui livelli di funzionalità della foresta, vedere "come generare Active Directory livelli di funzionalità del dominio e della foresta" nella Knowledge base della guida e del supporto tecnico all'indirizzo [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .</span><span class="sxs-lookup"><span data-stu-id="63f38-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 