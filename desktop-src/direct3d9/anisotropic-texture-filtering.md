---
description: La distorsione visibile nei texel di un oggetto 3D la cui superficie è orientata su un angolo rispetto al piano dello schermo è chiamata anisotropy.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtro trame anisotropo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363aeef463f137a240602e52410260108ee4a40a1a23da7b2e7c245ed6e74a65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676941"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtro trame anisotropo (Direct3D 9)

La distorsione visibile nei texel di un oggetto 3D la cui superficie è orientata su un angolo rispetto al piano dello schermo è chiamata anisotropy. Quando un pixel di una primitiva anisotropa viene mappato ai texel, la relativa forma viene distorta. Direct3D misura l'anisotropia di un pixel come l'allungamento, cio' la lunghezza divisa per larghezza, di un pixel dello schermo mappato inversamente nello spazio trame.

È possibile usare il filtro trame anisotropo in combinazione con il filtro trame lineare o il filtro delle trame mipmap per migliorare i risultati del rendering. L'applicazione abilita il filtro trame anisotropo chiamando il [**metodo IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Impostare il valore del primo parametro sul numero di indice intero (0-7) della trama per cui si sta selezionando un metodo di filtro trame. Passare D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER per il secondo parametro per impostare il filtro \_ \_ di ingrandimento, minificazione o mipmapping. Impostare il terzo parametro su D3DTEXF \_ ANISOTROP.

L'applicazione deve anche impostare il grado di anisotropia su un valore maggiore di uno. A tale scopo, chiamare il [**metodo IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Impostare il valore del primo parametro sul numero di indice intero (0-7) della trama per cui si sta impostando il grado di isotropia. Passare D3DSAMP \_ MAXANISOTROPY come valore del secondo parametro. Il parametro finale deve essere il grado di isotropia.

È possibile disabilitare il filtro isotropo impostando il grado di isotropia su uno; qualsiasi valore maggiore di uno lo abilita. Controllare il flag MaxAnisotropy nella struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare il possibile intervallo di valori per il grado di anisotropia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro trame](texture-filtering.md)
</dt> </dl>

 

 
