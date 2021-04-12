---
description: La modalità address texture mirror, identificata dal \_ membro mirror D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, fa sì che Direct3D rispecchi la trama a ogni limite intero.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modalità address texture mirror (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401167"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Modalità address texture mirror (Direct3D 9)

La modalità address texture mirror, identificata dal \_ membro mirror D3DTADDRESS del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fa sì che Direct3D rispecchi la trama a ogni limite intero. Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e specifichi le coordinate di trama (0,0, 0,0), (0.0, 3.0), (3.0, 3.0) e (3.0, 0,0). Impostando la modalità di indirizzamento della trama su D3DTADDRESS \_ mirror, la trama viene applicata tre volte nelle direzioni u-e-v. Ogni altra riga e colonna a cui viene applicato è un'immagine speculare della riga o della colonna precedente, come illustrato nella figura seguente.

![illustrazione delle immagini speculari in una griglia 3x3](images/mirror.png)

Gli effetti di questa modalità di indirizzamento della trama sono simili a quelli della modalità a capo, ma distinti. Per altre informazioni, vedere [modalità di indirizzamento della trama a capo (Direct3D 9)](wrap-texture-address-mode.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
