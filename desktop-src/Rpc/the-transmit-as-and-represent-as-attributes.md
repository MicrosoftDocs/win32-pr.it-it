---
title: Attributi transmit_as e represent_as
description: In questa sezione viene illustrata l'implementazione della conversione dei tipi di dati del programmatore utilizzando MIDL \ trasmettere \_ come \ e \ rappresentano \_ gli attributi \.
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872630"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="e4b4c-103">Trasmettere \_ come e rappresentare \_ gli attributi</span><span class="sxs-lookup"><span data-stu-id="e4b4c-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="e4b4c-104">In questa sezione viene illustrata l'implementazione della conversione dei tipi di dati del programmatore utilizzando MIDL **\[** [**Transmitte \_ come**](/windows/desktop/Midl/transmit-as) **\]** e **\[** [**\_ rappresentano**](/windows/desktop/Midl/represent-as) **\]** gli attributi.</span><span class="sxs-lookup"><span data-stu-id="e4b4c-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="e4b4c-105">La discussione è illustrata nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4b4c-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="e4b4c-106">Attributo **trasmissione \_ As**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="e4b4c-107">**Tipo per la funzione \_ \_ Xmit**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="e4b4c-108">**Tipo \_ dalla funzione \_ Xmit**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="e4b4c-109">Funzione **\_ \_ Xmit gratuita del tipo**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="e4b4c-110">Funzione **\_ \_ inst gratuita del tipo**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="e4b4c-111">**Rappresenta \_ come** attributo</span><span class="sxs-lookup"><span data-stu-id="e4b4c-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="e4b4c-112">Il **tipo denominato della funzione \_ \_ \_ locale**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="e4b4c-113">**Tipo denominato \_ \_ per \_** la funzione locale</span><span class="sxs-lookup"><span data-stu-id="e4b4c-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="e4b4c-114">Funzione **\_ locale del tipo denominato \_ Free \_**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="e4b4c-115">Funzione **\_ \_ \_ inst disponibile del tipo denominato**</span><span class="sxs-lookup"><span data-stu-id="e4b4c-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 