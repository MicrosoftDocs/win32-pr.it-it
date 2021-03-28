---
description: Il nome della funzione PatBlt (un'abbreviazione per il trasferimento di blocchi di pattern) implica che questa funzione replica semplicemente il pennello (o pattern) finché non riempie un rettangolo specificato.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Modello di trasferimento del blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993933"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="4c3b5-103">Modello di trasferimento del blocco</span><span class="sxs-lookup"><span data-stu-id="4c3b5-103">Pattern Block Transfer</span></span>

<span data-ttu-id="4c3b5-104">Il nome della funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (un'abbreviazione per il trasferimento di blocchi di pattern) implica che questa funzione replica semplicemente il pennello (o pattern) finché non riempie un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="4c3b5-105">Tuttavia, la funzione è in realtà molto più potente.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="4c3b5-106">Prima di replicare il pennello, combina i dati relativi al colore per il modello con i dati relativi al colore per i pixel esistenti sulla visualizzazione video usando un'operazione raster (POR).</span><span class="sxs-lookup"><span data-stu-id="4c3b5-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="4c3b5-107">Un por è un'operazione bit per bit applicata ai bit dei dati relativi al colore per il pennello replicato e ai bit dei dati relativi al colore per il rettangolo di destinazione sul dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="4c3b5-108">Sono presenti 256 ROPs; Tuttavia, la funzione **PatBlt** riconosce solo quelle che richiedono un modello e una destinazione (non quelle che richiedono un'origine).</span><span class="sxs-lookup"><span data-stu-id="4c3b5-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="4c3b5-109">La tabella seguente identifica il ROPs più comune.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="4c3b5-110">ROP</span><span class="sxs-lookup"><span data-stu-id="4c3b5-110">ROP</span></span>       | <span data-ttu-id="4c3b5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c3b5-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3b5-112">PATCOPY</span><span class="sxs-lookup"><span data-stu-id="4c3b5-112">PATCOPY</span></span>   | <span data-ttu-id="4c3b5-113">Copia il modello nella bitmap di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="4c3b5-114">PATINVERT</span><span class="sxs-lookup"><span data-stu-id="4c3b5-114">PATINVERT</span></span> | <span data-ttu-id="4c3b5-115">Combina la bitmap di destinazione con il modello utilizzando l'operatore booleano XOR.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="4c3b5-116">DSTINVERT</span><span class="sxs-lookup"><span data-stu-id="4c3b5-116">DSTINVERT</span></span> | <span data-ttu-id="4c3b5-117">Inverte la bitmap di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="4c3b5-118">NERO</span><span class="sxs-lookup"><span data-stu-id="4c3b5-118">BLACKNESS</span></span> | <span data-ttu-id="4c3b5-119">Converte tutti gli output in zeri binari.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="4c3b5-120">CANDORE</span><span class="sxs-lookup"><span data-stu-id="4c3b5-120">WHITENESS</span></span> | <span data-ttu-id="4c3b5-121">Converte tutti gli output in quelli binari.</span><span class="sxs-lookup"><span data-stu-id="4c3b5-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="4c3b5-122">Per altre informazioni, vedere [codici operativi raster](raster-operation-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4c3b5-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



