---
description: La modalità di wrapping dell'indirizzo della trama, identificata dal membro WRAP D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, fa in modo che Direct3D ripeta la trama in ogni giunzione \_ di interi.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Modalità indirizzo trama a capo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820273a68754c11f17f4f2762c7e824562b8e52bfc0b2b097c21e82789ce4168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627826"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Modalità indirizzo trama a capo (Direct3D 9)

La modalità di wrapping dell'indirizzo della trama, identificata dal membro WRAP D3DTADDRESS del tipo enumerato \_ [**D3DTEXTUREADDRESS,**](./d3dtextureaddress.md) fa in modo che Direct3D ripeta la trama in ogni giunzione di interi. Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e specifichi le coordinate di trama (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0). Impostando la modalità di indirizzamento della trama su D3DTADDRESS WRAP, la trama viene applicata tre volte in entrambe le direzioni u e v, come illustrato nella \_ figura seguente.

![illustrazione di una trama del viso incapsulata nella direzione u e nella direzione v](images/wrap.png)

Gli effetti di questa modalità dell'indirizzo di trama sono simili, ma diversi da quelli della modalità mirror. Per altre informazioni, vedere [Mirror Texture Address Mode (Direct3D 9) (Modalità indirizzo trama speculare -Direct3D 9).](mirror-texture-address-mode.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
