---
description: La modalità di indirizzamento della trama a capo, identificata dal \_ membro D3DTADDRESS wrap del tipo enumerato D3DTEXTUREADDRESS, consente a Direct3D di ripetere la trama in ogni giunzione di interi.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Modalità di indirizzamento della trama a capo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225332"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Modalità di indirizzamento della trama a capo (Direct3D 9)

La modalità di indirizzamento della trama a capo, identificata dal \_ membro D3DTADDRESS wrap del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , consente a Direct3D di ripetere la trama in ogni giunzione di interi. Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e specifichi le coordinate di trama (0,0, 0,0), (0.0, 3.0), (3.0, 3.0) e (3.0, 0,0). Impostando la modalità di indirizzamento della trama su D3DTADDRESS \_ wrap, la trama viene applicata tre volte nelle direzioni u-e-v, come illustrato nella figura seguente.

![illustrazione di una trama del volto racchiusa tra la direzione u e la direzione della v](images/wrap.png)

Gli effetti di questa modalità di indirizzamento della trama sono simili a, ma distinti da quelli della modalità mirror. Per ulteriori informazioni, vedere [modalità address texture mirror (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
