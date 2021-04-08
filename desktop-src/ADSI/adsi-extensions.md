---
title: Estensioni ADSI
description: Un'estensione ADSI è un oggetto COM speciale che consente a uno sviluppatore di estendere un oggetto ADSI.
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- Estensioni ADSI
- ADSI ADSI, utilizzo delle estensioni
- estensioni ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044079"
---
# <a name="adsi-extensions"></a><span data-ttu-id="9e40f-106">Estensioni ADSI</span><span class="sxs-lookup"><span data-stu-id="9e40f-106">ADSI Extensions</span></span>

<span data-ttu-id="9e40f-107">Un'estensione ADSI è un oggetto COM speciale che consente a uno sviluppatore di estendere un oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="9e40f-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="9e40f-108">Ogni estensione è associata a una classe specificata nella directory.</span><span class="sxs-lookup"><span data-stu-id="9e40f-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="9e40f-109">Con questo modello di estensione, gli sviluppatori possono aggiungere metodi per fornire un significato più dinamico a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e40f-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="9e40f-110">In un modello di programmazione di directory tradizionale, è possibile accedere a un oggetto ottenendo e impostando gli attributi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e40f-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="9e40f-111">Con le estensioni ADSI è possibile aggiungere altre funzionalità a un oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="9e40f-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="9e40f-112">In questa sezione vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e40f-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="9e40f-113">Vantaggi dell'utilizzo delle estensioni ADSI</span><span class="sxs-lookup"><span data-stu-id="9e40f-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="9e40f-114">Architettura dell'estensione ADSI</span><span class="sxs-lookup"><span data-stu-id="9e40f-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="9e40f-115">Come ADSI integra le estensioni</span><span class="sxs-lookup"><span data-stu-id="9e40f-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="9e40f-116">Che cosa Visualizza un client?</span><span class="sxs-lookup"><span data-stu-id="9e40f-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="9e40f-117">Recupero di interfacce ADSI dall'estensione</span><span class="sxs-lookup"><span data-stu-id="9e40f-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="9e40f-118">Librerie di tipi di estensione ADSI</span><span class="sxs-lookup"><span data-stu-id="9e40f-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="9e40f-119">Supporto per l'associazione anticipata</span><span class="sxs-lookup"><span data-stu-id="9e40f-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="9e40f-120">Supporto per l'associazione tardiva</span><span class="sxs-lookup"><span data-stu-id="9e40f-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="9e40f-121">Interfaccia IADsExtension</span><span class="sxs-lookup"><span data-stu-id="9e40f-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="9e40f-122">Supporto di interfacce duali o dispatch</span><span class="sxs-lookup"><span data-stu-id="9e40f-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="9e40f-123">Rivisitazione di regole di aggregazione COM con estensioni ADSI</span><span class="sxs-lookup"><span data-stu-id="9e40f-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="9e40f-124">Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia</span><span class="sxs-lookup"><span data-stu-id="9e40f-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="9e40f-125">Risoluzione dei conflitti di nome di funzione/proprietà nell'automazione nelle estensioni</span><span class="sxs-lookup"><span data-stu-id="9e40f-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




