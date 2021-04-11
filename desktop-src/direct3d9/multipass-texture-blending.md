---
description: Le applicazioni Direct3D possono ottenere numerosi effetti speciali applicando varie trame a una primitiva nel corso di più passaggi di rendering.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Combinazione di trame multipass (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124473"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Combinazione di trame multipass (Direct3D 9)

Le applicazioni Direct3D possono ottenere numerosi effetti speciali applicando varie trame a una primitiva nel corso di più passaggi di rendering. Il termine comune per questa operazione è la combinazione di trame MultiPASS. Un uso tipico della combinazione di trame MultiPASS consiste nell'emulare gli effetti dei modelli di illuminazione e ombreggiatura complessi applicando più colori da diverse trame diverse. Una di queste applicazioni è denominata Light Mapping. Per altre informazioni, vedere [mapping chiaro con trame (Direct3D 9)](light-mapping-with-textures.md).

> [!Note]  
> Alcuni dispositivi sono in grado di applicare più trame alle primitive in un singolo passaggio. Per informazioni dettagliate, vedere [blending di trame (Direct3D 9)](texture-blending.md).

 

Se l'hardware dell'utente non supporta la combinazione di più trame, l'applicazione può usare la combinazione di trame MultiPASS per ottenere gli stessi effetti visivi. Tuttavia, l'applicazione non può sostenere le frequenze dei fotogrammi possibili quando si usa la combinazione di più trame.

Per eseguire la fusione di trame MultiPASS in un'applicazione C/C++.

1.  Impostare una trama nella fase di trama 0 chiamando il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .
2.  Selezionare le operazioni e gli argomenti del colore e della fusione alfa desiderati con il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . Le impostazioni predefinite sono particolarmente adatte per la fusione di trame MultiPASS.
3.  Esegue il rendering degli oggetti appropriati nella scena.
4.  Impostare la trama successiva nella fase della trama 0.
5.  Impostare gli \_ Stati di rendering D3DRS SRCBLEND e D3DRS \_ DESTBLEND per modificare i fattori di fusione di origine e di destinazione in base alle esigenze. Il sistema combina le nuove trame con i pixel esistenti nella superficie di destinazione di rendering in base a questi parametri.
6.  Ripetere i passaggi 3, 4 e 5 con il numero di trame necessario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di trame](texture-blending.md)
</dt> </dl>

 

 
