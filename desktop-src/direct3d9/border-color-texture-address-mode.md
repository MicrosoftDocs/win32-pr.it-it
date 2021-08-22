---
description: La modalità di indirizzo della trama del colore del bordo, identificata dal membro BORDER D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, fa sì che Direct3D usi un colore arbitrario, noto come colore del bordo, per tutte le coordinate di trama esterne all'intervallo compreso tra \_ 0,0 e 1,0 inclusi.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modalità indirizzo trama colore bordo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e0685359227f80a847174157117e90116cffe8e61a48e172451a83aa8ec5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496317"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Modalità indirizzo trama colore bordo (Direct3D 9)

La modalità di indirizzo della trama del colore del bordo, identificata dal membro BORDER D3DTADDRESS del tipo enumerato \_ [**D3DTEXTUREADDRESS,**](./d3dtextureaddress.md) fa sì che Direct3D usi un colore arbitrario, noto come colore del bordo, per tutte le coordinate di trama esterne all'intervallo compreso tra 0,0 e 1,0 inclusi.

Nella figura seguente l'applicazione specifica che la trama deve essere applicata alla primitiva usando un bordo rosso.

![illustrazione di una trama e di una trama con un bordo rosso](images/border.png)

Le applicazioni impostano il colore del bordo chiamando [**IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Impostare il primo parametro per la chiamata all'identificatore della fase della trama desiderata, il secondo parametro sul valore dello stato della fase D3DSAMP BORDERCOLOR e il terzo parametro sul nuovo colore del bordo \_ RGBA.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
