---
title: Informazioni sull'oggetto di rete
description: Informazioni sull'oggetto di rete
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player,Oggetto Network
- Windows Media Player a oggetti, oggetto Network
- modello a oggetti,oggetto Di rete
- Windows Media Player ActiveX, oggetto Network
- ActiveX, oggetto Network
- Windows Media Player Controllo ActiveX mobile, oggetto Network
- Windows Media Player Mobile, oggetto Network
- Oggetto di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0378b1cd4469f6141a4ea60021f2d54e5c32b33ae1943624f7c65f70aa2a655f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903291"
---
# <a name="about-the-network-object"></a>Informazioni sull'oggetto di rete

**L'oggetto** Network regola le proprietà che consentono di determinare il livello di streaming del contenuto attraverso la rete. Ad esempio, è possibile determinare se i pacchetti vengono persi e intraprendere le azioni appropriate. **L'accesso** all'oggetto Network avviene solo tramite **la proprietà di** rete dell'oggetto **Player.** La **proprietà di** rete restituisce **l'oggetto** Network. È possibile accedere alle proprietà dell'oggetto **Rete** solo dopo che è stato creato. Ad esempio, per usare la **proprietà Bandwidth,** è necessario usare il codice seguente:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> <dt>

[**Modello a oggetti lettore per linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




