---
title: Protocollo WMPCD
description: Protocollo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolli
- Modello a oggetti di Windows Media Player, protocolli
- modello a oggetti, protocolli
- Controllo ActiveX di Windows Media Player, protocolli per il modello a oggetti
- Controllo ActiveX, protocolli per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, protocolli per il modello a oggetti
- Windows Media Player Mobile, protocolli per il modello a oggetti
- protocolli, modello a oggetti di Windows Media Player
- protocolli, WMPCD
- Protocollo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221379"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="d57e7-113">Protocollo WMPCD</span><span class="sxs-lookup"><span data-stu-id="d57e7-113">WMPCD Protocol</span></span>

<span data-ttu-id="d57e7-114">Il protocollo WMPCD consente di specificare tracce in un disco Compact usando la sintassi dell'URL.</span><span class="sxs-lookup"><span data-stu-id="d57e7-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="d57e7-115">Questa è la sintassi generale del protocollo:</span><span class="sxs-lookup"><span data-stu-id="d57e7-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="d57e7-116">Il segmento *unità* è l'indice dell'unità CD.</span><span class="sxs-lookup"><span data-stu-id="d57e7-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="d57e7-117">Il segmento *Track* è il numero della traccia. Nell'esempio seguente viene illustrato l'utilizzo del protocollo WMPCD.</span><span class="sxs-lookup"><span data-stu-id="d57e7-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="d57e7-118">Nell'esempio viene riprodotta la quarta traccia del disco nella prima unità CD (l'unità il cui indice è 0).</span><span class="sxs-lookup"><span data-stu-id="d57e7-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d57e7-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d57e7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d57e7-120">**Protocolli e tipi di file supportati**</span><span class="sxs-lookup"><span data-stu-id="d57e7-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




