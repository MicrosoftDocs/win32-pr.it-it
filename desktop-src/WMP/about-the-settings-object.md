---
title: Informazioni sull'oggetto Impostazioni
description: Informazioni sull'oggetto Impostazioni
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player,Impostazioni'oggetto
- Windows Media Player a oggetti, Impostazioni oggetto
- modello a oggetti, Impostazioni oggetto
- Windows Media Player ActiveX controllo, Impostazioni oggetto
- ActiveX, oggetto Impostazioni
- Windows Media Player Controllo ActiveX per dispositivi mobili, Impostazioni oggetto
- Windows Media Player Oggetto Mobile,Impostazioni
- Impostazioni oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74b8bd9db946a2915486647fa5831158198bef6115a34b6bb9fb81177f433de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583673"
---
# <a name="about-the-settings-object"></a>Informazioni sull'oggetto Impostazioni

**L Impostazioni o** object governa le impostazioni del controllo, ad esempio volume, numero di riproduzione, disattivazione dell'audio e così via. È possibile accedervi solo tramite la **Impostazioni** proprietà dell'oggetto **Player.** La **Impostazioni** proprietà restituisce **l'Impostazioni** oggetto . È possibile accedere alle proprietà dell'oggetto **Impostazioni** solo dopo che è stato creato. Ad esempio, per ottenere il valore della **proprietà Volume,** è necessario usare il codice seguente:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modello a oggetti lettore per linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 




