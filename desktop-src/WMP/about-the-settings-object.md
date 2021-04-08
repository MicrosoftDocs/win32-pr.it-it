---
title: Informazioni sull'oggetto Settings
description: Informazioni sull'oggetto Settings
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, oggetto Settings
- Modello a oggetti di Windows Media Player, oggetto Settings
- modello a oggetti, oggetto Settings
- Controllo ActiveX Windows Media Player, oggetto Settings
- Controllo ActiveX, oggetto Settings
- Controllo ActiveX Windows Media Player Mobile, oggetto Settings
- Windows Media Player Mobile, oggetto Settings
- Oggetto Settings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855569"
---
# <a name="about-the-settings-object"></a>Informazioni sull'oggetto Settings

L'oggetto **Settings** governa le impostazioni del controllo, ad esempio volume, Play Count, mute e così via. È accessibile solo tramite la proprietà **Settings** dell'oggetto **Player** . La proprietà **Settings** restituisce l'oggetto **Settings** . È possibile accedere alle proprietà dell'oggetto **Impostazioni** solo dopo averlo creato. Per ottenere, ad esempio, il valore della proprietà **volume** , è necessario usare il codice seguente:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 




