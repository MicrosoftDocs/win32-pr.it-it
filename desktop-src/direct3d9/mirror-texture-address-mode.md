---
description: La modalità di indirizzo della trama speculare, identificata dal membro D3DTADDRESS MIRROR del tipo enumerato D3DTEXTUREADDRESS, fa in modo che Direct3D rifletta la trama a ogni limite \_ integer.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modalità indirizzo trama speculare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ef8731c060e95c470bbf8d34222b9ee66e7f9da2c7a6f03a09c2989986ca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728368"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Modalità indirizzo trama speculare (Direct3D 9)

La modalità di indirizzo della trama speculare, identificata dal membro D3DTADDRESS MIRROR del tipo enumerato \_ [**D3DTEXTUREADDRESS,**](./d3dtextureaddress.md) fa in modo che Direct3D rifletta la trama a ogni limite integer. Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e specifichi le coordinate di trama (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0). Impostando la modalità di indirizzamento della trama su D3DTADDRESS MIRROR, la trama viene applicata tre volte in entrambe le direzioni \_ u e v. Ogni altra riga e colonna a cui viene applicata è un'immagine speculare della riga o della colonna precedente, come illustrato nella figura seguente.

![illustrazione di immagini speculari in una griglia 3x3](images/mirror.png)

Gli effetti di questa modalità di indirizzo di trama sono simili, ma distinti da quelli della modalità a capo automatico. Per altre informazioni, vedere [Wrap Texture Address Mode (Direct3D 9) (Eseguire il wrapping della modalità indirizzo trama -Direct3D 9).](wrap-texture-address-mode.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
