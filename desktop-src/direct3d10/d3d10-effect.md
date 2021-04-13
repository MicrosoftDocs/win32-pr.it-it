---
description: Queste costanti utilizzate quando si crea un effetto per definire il comportamento di compilazione o l'effetto di Runtime.
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: Costanti D3D10_EFFECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342161"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="bcc73-103">\_Costanti effetto D3D10</span><span class="sxs-lookup"><span data-stu-id="bcc73-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="bcc73-104">Queste costanti utilizzate quando si crea un effetto per definire il comportamento di compilazione o l'effetto di Runtime.</span><span class="sxs-lookup"><span data-stu-id="bcc73-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="bcc73-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="bcc73-105">\#define</span></span>                                 | <span data-ttu-id="bcc73-106">Valore</span><span class="sxs-lookup"><span data-stu-id="bcc73-106">Value</span></span>        | <span data-ttu-id="bcc73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcc73-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc73-108">\_ \_ \_ Effetto figlio compilazione effetto \_ D3D10</span><span class="sxs-lookup"><span data-stu-id="bcc73-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="bcc73-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="bcc73-109">1 << 0</span></span> | <span data-ttu-id="bcc73-110">Compilare il file con estensione FX in un effetto figlio.</span><span class="sxs-lookup"><span data-stu-id="bcc73-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="bcc73-111">Gli effetti figlio non hanno inizializzazioni per alcun valore condiviso perché vengono inizializzati nel pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="bcc73-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="bcc73-112">D3D10 \_ effetto \_ compilazione \_ Consenti \_ \_ operazioni lente</span><span class="sxs-lookup"><span data-stu-id="bcc73-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="bcc73-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="bcc73-113">1 << 1</span></span> | <span data-ttu-id="bcc73-114">Per impostazione predefinita, è abilitata la modalità prestazioni.</span><span class="sxs-lookup"><span data-stu-id="bcc73-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="bcc73-115">La modalità prestazioni non consente oggetti di stato modificabili impedendo la visualizzazione di espressioni non letterali nelle definizioni degli oggetti di stato.</span><span class="sxs-lookup"><span data-stu-id="bcc73-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="bcc73-116">Se si specifica questo flag, verrà disabilitata la modalità e gli oggetti di stato modificabili.</span><span class="sxs-lookup"><span data-stu-id="bcc73-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="bcc73-117">D3D10 \_ effetto \_ a \_ thread singolo</span><span class="sxs-lookup"><span data-stu-id="bcc73-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="bcc73-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="bcc73-118">1 << 3</span></span> | <span data-ttu-id="bcc73-119">Non tentare di eseguire la sincronizzazione con altri thread che caricano effetti nello stesso pool.</span><span class="sxs-lookup"><span data-stu-id="bcc73-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="bcc73-120">Queste costanti sono definite come macro in d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="bcc73-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcc73-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bcc73-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcc73-122">Costanti effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bcc73-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



