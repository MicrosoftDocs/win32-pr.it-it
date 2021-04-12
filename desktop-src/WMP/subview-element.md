---
title: Elemento subview
description: Elemento subview
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player Skin, elemento subview
- Skin, elemento subview
- Elemento subview
- riferimento per Skin, elemento subview
- elementi, visualizzazione subview
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331860"
---
# <a name="subview-element"></a>Elemento subview

L'elemento **subview** fornisce un modo per modificare una parte di un'interfaccia, ad esempio per fornire un pannello di controllo che può essere nascosto quando non è in uso. Gli elementi della **visualizzazione subview** sono sempre elementi figlio degli elementi di **visualizzazione** padre e possono contenere altro elemento Skin ad eccezione di **visualizzazione**, **tema** e altri elementi di **Sottovisualizzazione** .

L'elemento **subview** supporta gli attributi seguenti, definiti nell'elemento **View** .



| Attributo                                                       | Descrizione                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)                     | Specifica o Recupera il colore di sfondo del controllo di **Sottovisualizzazione** . Il valore predefinito è "None".        |
| [backgroundImage](view-backgroundimage.md)                     | Specifica o recupera l'immagine di sfondo del controllo **Sottovisualizzazione** .                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Specifica o recupera la quantità in base alla quale viene spostata la tonalità dell'immagine di sfondo.                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Specifica o Recupera il valore di saturazione dell'immagine di sfondo.                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | Specifica o recupera un valore che indica se l'immagine di sfondo del controllo **Sottovisualizzazione** è affiancata. |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Specifica o recupera un valore che indica se è possibile ridimensionare l'immagine di sfondo.                      |
| [transparencyColor](view-transparencycolor.md)                 | Specifica o Recupera il colore di trasparenza dell'immagine di sfondo.                                      |



 

L'elemento **subview** supporta gli attributi di ambiente, eccetto se specificato. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md).

L'elemento **subview** può implementare i gestori eventi di ambiente seguenti: [onendmove](onendmove.md) e [OnResize](onresize.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 




