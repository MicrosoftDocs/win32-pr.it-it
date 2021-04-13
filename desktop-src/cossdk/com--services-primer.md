---
description: COM+ fornisce un semplice modello di programmazione per l'utilizzo dei servizi automatici.
ms.assetid: 2d616b56-4b6a-4c3b-bbd8-d5ca03c4911f
title: Principali servizi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fd9d256b0213d3b1c58cae7d9670f87e4f4423
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342341"
---
# <a name="com-services-primer"></a><span data-ttu-id="a2b7f-103">Principali servizi COM+</span><span class="sxs-lookup"><span data-stu-id="a2b7f-103">COM+ Services Primer</span></span>

<span data-ttu-id="a2b7f-104">COM+ fornisce un semplice modello di programmazione per l'utilizzo dei servizi automatici.</span><span class="sxs-lookup"><span data-stu-id="a2b7f-104">COM+ provides a simple programming model for using its automatic services.</span></span> <span data-ttu-id="a2b7f-105">È possibile semplicemente impostare questi servizi come attributi dichiarativi sui componenti e sui relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="a2b7f-105">You can simply set these services as declarative attributes on components and their methods.</span></span> <span data-ttu-id="a2b7f-106">Quando si impostano questi attributi, COM+ recapita automaticamente i servizi richiesti all'oggetto in modo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2b7f-106">When you set these attributes, COM+ automatically delivers the requested services to the object as required.</span></span>

<span data-ttu-id="a2b7f-107">Questa introduzione Mostra i servizi COM+ in azione esaminando il codice del componente di esempio in tre passaggi definiti.</span><span class="sxs-lookup"><span data-stu-id="a2b7f-107">This primer shows COM+ services in action by walking through sample component code in three defined steps.</span></span> <span data-ttu-id="a2b7f-108">La complessità delle informazioni si basa sulle fasi di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a2b7f-108">The complexity of the information builds as the steps progress.</span></span> <span data-ttu-id="a2b7f-109">Il codice è incentrato sul modello di programmazione semplificato, usando l'elaborazione delle transazioni per illustrare i principi COM+ di base.</span><span class="sxs-lookup"><span data-stu-id="a2b7f-109">The code focuses on the simplified programming model, using transaction processing to demonstrate basic COM+ principles.</span></span>

<span data-ttu-id="a2b7f-110">Ognuno dei passaggi seguenti illustra un aspetto fondamentale dei servizi COM+:</span><span class="sxs-lookup"><span data-stu-id="a2b7f-110">Each of the following steps illustrates a fundamental aspect of COM+ services:</span></span>

-   [<span data-ttu-id="a2b7f-111">Passaggio 1: creazione di un componente transazionale</span><span class="sxs-lookup"><span data-stu-id="a2b7f-111">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
-   [<span data-ttu-id="a2b7f-112">Passaggio 2: estensione di una transazione tra più componenti</span><span class="sxs-lookup"><span data-stu-id="a2b7f-112">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
-   [<span data-ttu-id="a2b7f-113">Passaggio 3: riutilizzo dei componenti</span><span class="sxs-lookup"><span data-stu-id="a2b7f-113">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)

## <a name="related-topics"></a><span data-ttu-id="a2b7f-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2b7f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2b7f-115">Panoramica della programmazione COM+</span><span class="sxs-lookup"><span data-stu-id="a2b7f-115">COM+ Programming Overview</span></span>](com--programming-overview.md)
</dt> <dt>

[<span data-ttu-id="a2b7f-116">Panoramica dell'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="a2b7f-116">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> <dt>

[<span data-ttu-id="a2b7f-117">Configurazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="a2b7f-117">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="a2b7f-118">Contesti COM+ e modelli di threading</span><span class="sxs-lookup"><span data-stu-id="a2b7f-118">COM+ Contexts and Threading Models</span></span>](com--contexts-and-threading-models.md)
</dt> <dt>

[<span data-ttu-id="a2b7f-119">Creazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="a2b7f-119">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="a2b7f-120">Progettazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="a2b7f-120">Designing COM+ Applications</span></span>](designing-com--applications.md)
</dt> </dl>

 

 



