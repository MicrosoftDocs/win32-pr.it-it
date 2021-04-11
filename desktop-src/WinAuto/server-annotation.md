---
title: Annotazione server
description: In questa sezione vengono fornite informazioni sull'utilizzo delle annotazioni server.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044324"
---
# <a name="server-annotation"></a><span data-ttu-id="036d4-103">Annotazione server</span><span class="sxs-lookup"><span data-stu-id="036d4-103">Server Annotation</span></span>

<span data-ttu-id="036d4-104">In questa sezione vengono fornite informazioni sull'utilizzo delle annotazioni server.</span><span class="sxs-lookup"><span data-stu-id="036d4-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="036d4-105">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="036d4-105">Summary</span></span>

<span data-ttu-id="036d4-106">Si definisce una classe che implementa [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), ne crea un'istanza e si indica al sistema che si desidera che esegua l'override di proprietà specifiche su elementi dell'interfaccia utente specifici.</span><span class="sxs-lookup"><span data-stu-id="036d4-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="036d4-107">Quando un client richiede una delle proprietà di uno degli elementi dell'interfaccia utente, viene chiamato l'oggetto e viene data la possibilità di fornire un valore.</span><span class="sxs-lookup"><span data-stu-id="036d4-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="036d4-108">Se l'oggetto restituisce un valore, tale valore viene passato nuovamente al client.</span><span class="sxs-lookup"><span data-stu-id="036d4-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="036d4-109">Se l'oggetto non restituisce un valore, il valore predefinito per tale elemento dell'interfaccia utente viene restituito al client.</span><span class="sxs-lookup"><span data-stu-id="036d4-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="036d4-110">Quando usare questa tecnica</span><span class="sxs-lookup"><span data-stu-id="036d4-110">When to Use This Technique</span></span>

<span data-ttu-id="036d4-111">Utilizzare questa tecnica quando si desidera eseguire l'override delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="036d4-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="036d4-112">Questa tecnica è molto più semplice rispetto alle tecniche **IAccessible** precedenti.</span><span class="sxs-lookup"><span data-stu-id="036d4-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="036d4-113">Per ulteriori informazioni, vedere [alternative all'annotazione dinamica](alternatives-to-dynamic-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="036d4-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="036d4-114">Non è possibile utilizzare l'annotazione server per modificare la struttura dell'oggetto esposto.</span><span class="sxs-lookup"><span data-stu-id="036d4-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="036d4-115">Per modificare la struttura di un oggetto, è necessario implementare un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.</span><span class="sxs-lookup"><span data-stu-id="036d4-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="036d4-116">Per ulteriori informazioni sull'annotazione del server, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="036d4-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="036d4-117">Uso dell'annotazione server</span><span class="sxs-lookup"><span data-stu-id="036d4-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="036d4-118">Esempio di annotazione server</span><span class="sxs-lookup"><span data-stu-id="036d4-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




