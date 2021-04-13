---
description: La modalità di indirizzamento dei colori del bordo, identificata dal \_ membro del bordo D3DTADDRESS del tipo enumerato D3DTEXTUREADDRESS, induce Direct3D a usare un colore arbitrario, noto come colore del bordo, per qualsiasi coordinate di trama non compresa nell'intervallo tra 0,0 e 1,0 inclusi.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modalità di indirizzo della trama colore del bordo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401482"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Modalità di indirizzo della trama colore del bordo (Direct3D 9)

La modalità di indirizzamento dei colori del bordo, identificata dal \_ membro del bordo D3DTADDRESS del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , induce Direct3D a usare un colore arbitrario, noto come colore del bordo, per qualsiasi coordinate di trama non compresa nell'intervallo tra 0,0 e 1,0 inclusi.

Nell'illustrazione seguente, l'applicazione specifica che la trama viene applicata alla primitiva usando un bordo rosso.

![illustrazione di una trama e una trama con un bordo rosso](images/border.png)

Le applicazioni impostano il colore del bordo chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate). Impostare il primo parametro per la chiamata all'identificatore della fase di trama desiderato, il secondo parametro per il \_ valore dello stato della fase BorderColor D3DSAMP e il terzo parametro al nuovo colore del bordo di RGBA.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di indirizzamento delle trame](texture-addressing-modes.md)
</dt> </dl>

 

 
