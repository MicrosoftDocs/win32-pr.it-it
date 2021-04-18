---
description: I tipi di formato testo dei dati configurabili possono essere stringhe di testo di qualsiasi lunghezza. I valori null incorporati non sono consentiti.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipi di formato testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319426"
---
# <a name="text-format-types"></a><span data-ttu-id="7d0c5-104">Tipi di formato testo</span><span class="sxs-lookup"><span data-stu-id="7d0c5-104">Text Format Types</span></span>

<span data-ttu-id="7d0c5-105">I tipi di formato testo dei dati configurabili possono essere stringhe di testo di qualsiasi lunghezza.</span><span class="sxs-lookup"><span data-stu-id="7d0c5-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="7d0c5-106">I valori null incorporati non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="7d0c5-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="7d0c5-107">Sono disponibili i seguenti tipi di formato testo:</span><span class="sxs-lookup"><span data-stu-id="7d0c5-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="7d0c5-108">Testo arbitrario</span><span class="sxs-lookup"><span data-stu-id="7d0c5-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="7d0c5-109">RTF</span><span class="sxs-lookup"><span data-stu-id="7d0c5-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="7d0c5-110">Formattato</span><span class="sxs-lookup"><span data-stu-id="7d0c5-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="7d0c5-111">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="7d0c5-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="7d0c5-112">Tipo di identificatore</span><span class="sxs-lookup"><span data-stu-id="7d0c5-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="7d0c5-113">Gli elementi configurabili del tipo di formato testo vengono utilizzati in campi di database non binari e in generale potrebbero essere sostituiti da qualsiasi stringa di qualsiasi lunghezza.</span><span class="sxs-lookup"><span data-stu-id="7d0c5-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="7d0c5-114">Tuttavia, particolari elementi configurabili presentano anche restrizioni semantiche.</span><span class="sxs-lookup"><span data-stu-id="7d0c5-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="7d0c5-115">Ad esempio, un elemento configurabile che è necessario per essere una chiave esterna in una tabella specifica presenta restrizioni semantiche aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="7d0c5-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="7d0c5-116">Tali restrizioni semantiche non vengono applicate da Mergemod.dll e pertanto gli autori dei moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="7d0c5-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



