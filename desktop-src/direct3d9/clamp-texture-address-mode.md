---
description: La modalità dell'indirizzo della trama di collegamento, identificata dal membro CLAMP D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, fa sì che Direct3D attasi le coordinate della trama all'intervallo \_ \[ 0.0, 1.0. \]
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Impostazione della modalità indirizzo trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0602b66c28dfbd48cc7ac3504ff643cd0ffe31769ee8edbeede5b4b870914289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751357"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Impostazione della modalità indirizzo trama (Direct3D 9)

La modalità dell'indirizzo della trama di collegamento, identificata dal membro CLAMP D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, fa sì che Direct3D attasi le coordinate della trama all'intervallo \_ [](./d3dtextureaddress.md) \[ 0.0, 1.0. \] In altri modo, applica la trama una sola volta, quindi spalma il colore dei pixel del bordo. Si supponga, ad esempio, che l'applicazione crei una primitiva quadrata e assegni le coordinate di trama (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0) ai vertici della primitiva. Se si imposta la modalità di indirizzamento della trama su D3DTADDRESS \_ CLAMP, la trama viene applicata una sola volta. I colori in pixel nella parte superiore delle colonne e alla fine delle righe vengono estesi rispettivamente all'inizio e alla destra della primitiva.

La figura seguente mostra una trama con chiusura.

![illustrazione di una trama e di una trama con chiusura](images/clamp.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
