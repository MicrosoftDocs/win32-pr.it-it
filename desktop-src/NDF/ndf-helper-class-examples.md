---
title: Esempi di estensione della classe helper NDF
description: Questi esempi si applicano solo quando gli sviluppatori ritengono che sia necessario estendere la funzionalità di una classe helper Microsoft NDF dichiarata come estendibile.
ms.assetid: 048e42f5-66d8-41c6-9e97-8da68c9ad151
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3ecf34bb8e90aad8c28f582860d44e81706e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707072"
---
# <a name="ndf-helper-class-extension-examples"></a><span data-ttu-id="5ef7e-103">Esempi di estensione della classe helper NDF</span><span class="sxs-lookup"><span data-stu-id="5ef7e-103">NDF Helper Class Extension Examples</span></span>

<span data-ttu-id="5ef7e-104">Questi esempi si applicano solo quando gli sviluppatori ritengono che sia necessario estendere la funzionalità di una classe helper Microsoft NDF dichiarata come estendibile.</span><span class="sxs-lookup"><span data-stu-id="5ef7e-104">These examples apply only when developers believe it is necessary to extend the functionality of a Microsoft NDF Helper Class that is declared to be extensible.</span></span> <span data-ttu-id="5ef7e-105">Questa operazione in genere non è necessaria, ma in alcuni casi le opportunità di diagnostica univoche si presentano a causa dei requisiti hardware o software specifici del componente.</span><span class="sxs-lookup"><span data-stu-id="5ef7e-105">This is generally not necessary, but in some cases, unique diagnostic opportunities present themselves because of the specific hardware or software requirements of the component.</span></span>

<span data-ttu-id="5ef7e-106">I due esempi seguenti sono correlati e il primo deve essere compreso prima di analizzare il secondo.</span><span class="sxs-lookup"><span data-stu-id="5ef7e-106">The two examples that follow are related and the first should be understood before analyzing the second.</span></span> <span data-ttu-id="5ef7e-107">Il primo fornisce un'implementazione di un' [estensione della classe helper NDF](ndf-helper-class-example.md) usando una classe denominata SimpleHelperFileClass.</span><span class="sxs-lookup"><span data-stu-id="5ef7e-107">The first provides an implementation of an [NDF Helper Class Extension](ndf-helper-class-example.md) using a class called SimpleHelperFileClass.</span></span>

<span data-ttu-id="5ef7e-108">La seconda [estensione della classe helper NDF con](ndf-helper-class-example-with-handoff.md)la consegna, fornisce un esempio di estensione che non esegue attività diagnostiche specifiche, ma genera solo un'ipotesi di integrità bassa per SimpleHelperFileClass nel primo esempio.</span><span class="sxs-lookup"><span data-stu-id="5ef7e-108">The second, [NDF Helper Class Extension with Handoff](ndf-helper-class-example-with-handoff.md), provides an example of an extension that does not perform specific diagnostic tasks but only generates a low health hypothesis for the SimpleHelperFileClass in the first example.</span></span>

 

 




