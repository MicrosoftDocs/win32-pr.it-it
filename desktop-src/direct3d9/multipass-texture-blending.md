---
description: Le applicazioni Direct3D possono ottenere numerosi effetti speciali applicando varie trame a una primitiva nel corso di più passaggi di rendering.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Fusione di trame multipass (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ec4916cb3c86c0e3aa6e2c6ab9a5e03de8304989391b9c80b1070fc7b51594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491521"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Fusione di trame multipass (Direct3D 9)

Le applicazioni Direct3D possono ottenere numerosi effetti speciali applicando varie trame a una primitiva nel corso di più passaggi di rendering. Il termine comune è la fusione di trame a più passa. Un uso tipico della fusione di trame multipass consiste nell'emulare gli effetti di modelli di illuminazione e ombreggiatura complessi applicando più colori da diverse trame. Una di queste applicazioni è denominata mapping della luce. Per altre informazioni, vedere [Mapping di luce con trame (Direct3D 9).](light-mapping-with-textures.md)

> [!Note]  
> Alcuni dispositivi sono in grado di applicare più trame alle primitive in un unico passaggio. Per informazioni dettagliate, [vedere Texture Blending (Direct3D 9) (Fusione delle trame (Direct3D 9).](texture-blending.md)

 

Se l'hardware dell'utente non supporta la fusione di più trame, l'applicazione può usare la fusione di trame multipass per ottenere gli stessi effetti visivi. Tuttavia, l'applicazione non può sostenere le frequenze dei fotogrammi possibili quando si usa la fusione di più trame.

Per eseguire la fusione di trame multipass in un'applicazione C/C++.

1.  Impostare una trama nella fase della trama 0 chiamando il [**metodo IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)
2.  Selezionare gli argomenti e le operazioni di fusione alfa e colore desiderati con [**il metodo IDirect3DDevice9::SetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) Le impostazioni predefinite sono particolarmente adatte per la fusione di trame multipass.
3.  Eseguire il rendering degli oggetti appropriati nella scena.
4.  Impostare la trama successiva nella fase trama 0.
5.  Impostare gli stati di rendering D3DRS \_ SRCBLEND e D3DRS DESTBLEND per modificare i fattori di fusione di origine e \_ destinazione in base alle esigenze. Il sistema combina le nuove trame con i pixel esistenti nella superficie di destinazione di rendering in base a questi parametri.
6.  Ripetere i passaggi 3, 4 e 5 con tutte le trame necessarie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione delle trame](texture-blending.md)
</dt> </dl>

 

 
