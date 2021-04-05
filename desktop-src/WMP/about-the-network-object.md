---
title: Informazioni sull'oggetto di rete
description: Informazioni sull'oggetto di rete
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player, oggetto di rete
- Modello a oggetti di Windows Media Player, oggetto di rete
- modello a oggetti, oggetto di rete
- Controllo ActiveX Windows Media Player, oggetto di rete
- Controllo ActiveX, oggetto di rete
- Controllo ActiveX Windows Media Player Mobile, oggetto di rete
- Windows Media Player Mobile, oggetto di rete
- Oggetto di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707801"
---
# <a name="about-the-network-object"></a><span data-ttu-id="b4445-111">Informazioni sull'oggetto di rete</span><span class="sxs-lookup"><span data-stu-id="b4445-111">About the Network Object</span></span>

<span data-ttu-id="b4445-112">L'oggetto di **rete** regola le proprietà che consentono di determinare la modalità di trasmissione del contenuto attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="b4445-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="b4445-113">Ad esempio, è possibile verificare se i pacchetti vengono persi e intraprendere l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="b4445-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="b4445-114">È possibile accedere all'oggetto di **rete** solo tramite la proprietà **Network** dell'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="b4445-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="b4445-115">La proprietà di **rete** restituisce l'oggetto di **rete** .</span><span class="sxs-lookup"><span data-stu-id="b4445-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="b4445-116">È possibile accedere solo alle proprietà dell'oggetto di **rete** dopo averla creata.</span><span class="sxs-lookup"><span data-stu-id="b4445-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="b4445-117">Ad esempio, per usare la proprietà **Bandwidth** , è necessario usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="b4445-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="b4445-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4445-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4445-119">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="b4445-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="b4445-120">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="b4445-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




