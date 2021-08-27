---
title: Origine immagine thumb
description: Origine immagine thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Skin per dispositivi mobili, trackbar
- skin, trackbar
- informazioni di riferimento su skin, trackbar
- trackbar nelle skin, origine immagine
- trackbar nelle skin, origine immagine thumb
- origine immagine per skin, trackbar
- thumb,image source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550569a2858ba283824f28f6793097caa140c6112bccc41b3423413e17b6d89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122771"
---
# <a name="thumb-image-source"></a>Origine immagine thumb

È necessario definire il nome del file che contiene l'immagine thumb. Deve essere un nome di file valido con l'estensione .bmp, .gif, .jpg o .png. Il file deve contenere tre immagini affiancate di dimensioni identiche. Devono essere adiacenti tra loro senza spazio tra. La posizione in alto a sinistra dell'immagine a sinistra deve essere nell'angolo superiore sinistro del file. L'immagine sul lato sinistro è l'immagine normale per l'immagine del cursore e l'immagine al centro rappresenta lo stato di push e l'immagine a destra rappresenta lo stato disabilitato.


```C++
SeekThumb.bmp

```



È possibile rendere trasparenti determinate aree dell'immagine del cursore. In questo modo sarà possibile creare immagini thumb in forme diverse da rettangolari. Qualsiasi area dell'immagine thumb riempita con il colore specificato dal valore RGB 255, 0, 255 sarà trasparente nell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Trackbar**](trackbars.md)
</dt> </dl>

 

 




