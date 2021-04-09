---
title: Origine immagine Thumb
description: Origine immagine Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, trackbars
- interfacce, TrackBar
- riferimento per Skin, trackbars
- TrackBar in interfacce, origine immagine
- TrackBar in Skin, origine immagine Thumb
- origine immagine per Skin, trackbars
- Thumb, origine immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044376"
---
# <a name="thumb-image-source"></a>Origine immagine Thumb

È necessario definire il nome del file che contiene l'immagine Thumb. Deve essere un nome di file valido con estensione bmp, gif, jpg o png. Il file deve contenere tre immagini side-by-side di dimensioni identiche. Devono essere adiacenti tra loro senza spazi. La posizione superiore sinistra dell'immagine di sinistra deve essere nell'angolo superiore sinistro del file. L'immagine a sinistra è l'immagine normale per l'immagine del cursore e l'immagine al centro raffigura lo stato di push e l'immagine a destra illustra lo stato disabilitato.


```C++
SeekThumb.bmp

```



Potrebbe essere necessario rendere trasparente alcune aree dell'immagine Thumb. Ciò consentirà di creare immagini Thumb in forme diverse da rettangolare. Qualsiasi area dell'immagine Thumb riempita con il colore specificato dal valore RGB 255, 0, 255 verrà visualizzata trasparente nell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**TrackBar**](trackbars.md)
</dt> </dl>

 

 




