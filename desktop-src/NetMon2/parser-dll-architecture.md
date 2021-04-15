---
description: L'architettura della DLL del parser deve fornire le funzionalità illustrate nella figura seguente.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architettura DLL parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485853"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="01923-103">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="01923-103">Parser DLL Architecture</span></span>

<span data-ttu-id="01923-104">L'architettura della DLL del parser deve fornire le funzionalità illustrate nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="01923-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="01923-105">Tenere presente che alcune funzionalità richiedono l'implementazione di un solo punto di ingresso.</span><span class="sxs-lookup"><span data-stu-id="01923-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="01923-106">Tuttavia, se la DLL del parser supporta più protocolli, la funzionalità richiede l'implementazione di più punti di ingresso.</span><span class="sxs-lookup"><span data-stu-id="01923-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![funzionalità dll del parser](images/parserarchitecture1.png)



| <span data-ttu-id="01923-108">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="01923-108">For information about</span></span>                                                  | <span data-ttu-id="01923-109">Vedere</span><span class="sxs-lookup"><span data-stu-id="01923-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="01923-110">Come implementare le funzioni di esportazione della DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="01923-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="01923-111">Scrittura di un parser di protocollo</span><span class="sxs-lookup"><span data-stu-id="01923-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="01923-112">Funzioni e strutture specifiche utilizzate dai parser, ovvero argomenti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="01923-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="01923-113">Funzioni e strutture del parser</span><span class="sxs-lookup"><span data-stu-id="01923-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



