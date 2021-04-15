---
description: La distorsione visibile nei Texel di un oggetto 3D la cui superficie è orientata a un angolo rispetto al piano dello schermo è detta anisotropia.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtro di trama anisotropico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483749"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtro di trama anisotropico (Direct3D 9)

La distorsione visibile nei Texel di un oggetto 3D la cui superficie è orientata a un angolo rispetto al piano dello schermo è detta anisotropia. Quando viene eseguito il mapping di un pixel di una primitiva anisotropico a Texel, la relativa forma viene distorta. Direct3D misura l'anisotropia di un pixel come allungamento, ovvero la lunghezza divisa per larghezza, di un pixel dello schermo che è mappato in senso inverso nello spazio della trama.

È possibile usare il filtro di trama anisotropico insieme al filtro di trama lineare o al filtro della trama mipmap per migliorare i risultati del rendering. L'applicazione Abilita il filtro di trama anisotropico chiamando il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Impostare il valore del primo parametro sul numero di indice Integer (0-7) della trama per cui si seleziona un metodo di filtro della trama. Passare D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER per il secondo parametro per impostare il filtro di ingrandimento, minification o mapping MIP. Impostare il terzo parametro su D3DTEXF \_ anisotropico.

L'applicazione deve inoltre impostare il grado di anisotropia su un valore maggiore di uno. A tale scopo, chiamare il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Impostare il valore del primo parametro sul numero di indice Integer (0-7) della trama per cui si sta impostando il livello di isotropia. Passare D3DSAMP \_ MAXANISOTROPY come valore del secondo parametro. Il parametro finale deve essere il livello di isotropia.

È possibile disabilitare il filtro di applicazione del filtro di base impostando il grado di isotropia su uno. qualsiasi valore maggiore di uno lo Abilita. Controllare il flag MaxAnisotropy nella struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare il possibile intervallo di valori per il grado di anisotropia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtraggio trama](texture-filtering.md)
</dt> </dl>

 

 
