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
# <a name="about-the-network-object"></a>Informazioni sull'oggetto di rete

L'oggetto di **rete** regola le proprietà che consentono di determinare la modalità di trasmissione del contenuto attraverso la rete. Ad esempio, è possibile verificare se i pacchetti vengono persi e intraprendere l'azione appropriata. È possibile accedere all'oggetto di **rete** solo tramite la proprietà **Network** dell'oggetto **Player** . La proprietà di **rete** restituisce l'oggetto di **rete** . È possibile accedere solo alle proprietà dell'oggetto di **rete** dopo averla creata. Ad esempio, per usare la proprietà **Bandwidth** , è necessario usare il codice seguente:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




