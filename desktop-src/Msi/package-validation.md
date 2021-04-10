---
description: Prima di tentare di installare il pacchetto per la prima volta, è consigliabile eseguire la convalida su ogni pacchetto di installazione nuovo o appena modificato.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Convalida del pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880725"
---
# <a name="package-validation"></a><span data-ttu-id="99b55-103">Convalida del pacchetto</span><span class="sxs-lookup"><span data-stu-id="99b55-103">Package Validation</span></span>

<span data-ttu-id="99b55-104">Prima di tentare di installare il pacchetto per la prima volta, è consigliabile eseguire la convalida su ogni pacchetto di installazione nuovo o appena modificato.</span><span class="sxs-lookup"><span data-stu-id="99b55-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="99b55-105">La convalida del pacchetto include i tre processi seguenti:</span><span class="sxs-lookup"><span data-stu-id="99b55-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="99b55-106">Convalida interna</span><span class="sxs-lookup"><span data-stu-id="99b55-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="99b55-107">Convalida del pool di stringhe</span><span class="sxs-lookup"><span data-stu-id="99b55-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="99b55-108">Analizzatori di coerenza interni-CIEM</span><span class="sxs-lookup"><span data-stu-id="99b55-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="99b55-109">I moduli merge devono essere convalidati tramite il metodo descritto in [convalida dei moduli unione](validating-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="99b55-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="99b55-110">Evalcom2.dll fornisce un oggetto COM che implementa le operazioni di convalida per i pacchetti di installazione e i moduli unione.</span><span class="sxs-lookup"><span data-stu-id="99b55-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="99b55-111">L'oggetto Main implementa le interfacce per i programmi C/C++.</span><span class="sxs-lookup"><span data-stu-id="99b55-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="99b55-112">Per altre informazioni, vedere [automazione della convalida](validation-automation.md).</span><span class="sxs-lookup"><span data-stu-id="99b55-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 



