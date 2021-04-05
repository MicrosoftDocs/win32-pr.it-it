---
title: " define"
description: La direttiva \ define assegna il valore specificato al nome specificato. Tutte le occorrenze successive del nome vengono sostituite dal valore.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711950"
---
# <a name="define"></a><span data-ttu-id="892bc-104">\#definire</span><span class="sxs-lookup"><span data-stu-id="892bc-104">\#define</span></span>

<span data-ttu-id="892bc-105">La direttiva **\# define** assegna il valore specificato al nome specificato.</span><span class="sxs-lookup"><span data-stu-id="892bc-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="892bc-106">Tutte le occorrenze successive del nome vengono sostituite dal valore.</span><span class="sxs-lookup"><span data-stu-id="892bc-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="892bc-107"><span id="name"></span><span id="NAME"></span>*nome*</span><span class="sxs-lookup"><span data-stu-id="892bc-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="892bc-108">Nome da definire.</span><span class="sxs-lookup"><span data-stu-id="892bc-108">Name to be defined.</span></span> <span data-ttu-id="892bc-109">Questo valore è costituito da qualsiasi combinazione di lettere, cifre e punteggiatura valida per il preprocessore C/C++.</span><span class="sxs-lookup"><span data-stu-id="892bc-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="892bc-110"><span id="value"></span><span id="VALUE"></span>*valore*</span><span class="sxs-lookup"><span data-stu-id="892bc-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="892bc-111">Integer, stringa di caratteri o riga di testo.</span><span class="sxs-lookup"><span data-stu-id="892bc-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="892bc-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="892bc-112">Example</span></span>

<span data-ttu-id="892bc-113">In questo esempio i valori vengono assegnati ai nomi diversi da ZERO e USERCLASS:</span><span class="sxs-lookup"><span data-stu-id="892bc-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="892bc-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="892bc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892bc-115">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="892bc-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




