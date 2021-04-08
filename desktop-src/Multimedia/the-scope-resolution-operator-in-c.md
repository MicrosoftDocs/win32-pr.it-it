---
title: Operatore di risoluzione dell'ambito in C++
description: Operatore di risoluzione dell'ambito in C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856202"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="c85c7-103">Operatore di risoluzione dell'ambito in C++</span><span class="sxs-lookup"><span data-stu-id="c85c7-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="c85c7-104">Due due punti (::) vengono usati in C++ come operatore di *risoluzione dell'ambito* .</span><span class="sxs-lookup"><span data-stu-id="c85c7-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="c85c7-105">Questo operatore offre una maggiore libertà di denominazione delle variabili, consentendo di distinguere le variabili con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="c85c7-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="c85c7-106">Ad esempio, *MyFile:: Read* si riferisce al metodo *Read* della classe *MyFile* di oggetti, invece di *YourFile:: Read*, che fa riferimento a un metodo *Read* nella classe *YourFile* .</span><span class="sxs-lookup"><span data-stu-id="c85c7-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




