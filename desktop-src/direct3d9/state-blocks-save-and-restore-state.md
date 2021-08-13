---
description: Un blocco di stato è un gruppo di stati del dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Blocchi di stato Salvataggio e ripristino dello stato (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a56ed6490b0d81b7e643ef892e6a760f00b841531bd21dc69a4069f07b9aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291728"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Blocchi di stato Salvataggio e ripristino dello stato (Direct3D 9)

Un blocco di stato è un gruppo di stati del dispositivo. Lo stato del dispositivo è costituito da stato di rendering, stato vertice, stato pixel o tutti gli elementi precedenti. Un blocco di stato contiene uno snapshot dello stato corrente di un dispositivo oppure è possibile creare un blocco di stato che registra ogni modifica di stato apportata dall'applicazione.

## <a name="capture-a-block-of-state"></a>Acquisire un blocco di stato

Scegliere il tipo di stato da acquisire e creare un blocco di stato simile al seguente:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) crea un blocco di stato e acquisisce automaticamente lo stato del dispositivo. Lo stato del dispositivo viene specificato dal tipo di blocco di stato nel primo argomento. Questo stato può essere uno dei seguenti: tutti gli stati del dispositivo (vedere Salvataggio di tutti gli stati del dispositivo con [stateBlock (Direct3D 9),](saving-all-device-states-with-a-stateblock.md)tutti gli stati pixel (vedere Salvataggio dello stato dei pixel con [uno stateBlock (Direct3D 9) )](saving-pixel-states-with-a-stateblock.md)o tutti gli stati dei vertici (vedere Salvataggio degli stati dei vertici con [uno stateBlock (Direct3D 9).](saving-vertex-states-with-a-stateblock.md)

Il sistema di effetti usa un blocco di stato per salvare lo stato. Dopo [**la chiamata a ID3DXEffect::Begin,**](id3dxeffect--begin.md) viene creato un blocco di stato e viene acquisito lo stato. Quando [**viene chiamato ID3DXEffect::End,**](id3dxeffect--end.md) lo stato del blocco di stato viene riapplicato al dispositivo.

## <a name="capture-individual-states"></a>Acquisire singoli stati

Per salvare una sequenza di stato personalizzata, eseguire il wrapping dello stato che si vuole salvare in una coppia [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) e [**IDirect3DDevice9::EndStateBlock.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) BeginStateBlock indica al dispositivo corrente di configurare un blocco di stato e aggiungerlo a ogni modifica di stato che si verifica fino a quando non viene chiamato EndStateBlock. Ecco un esempio:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



In questo modo, qualsiasi numero di modifiche di stato in qualsiasi sequenza verrà salvato in un blocco di stato personalizzato. Successivamente, quando si vuole usare il blocco di stato per reimpostare lo stato del dispositivo, chiamare [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Verrà sovrascritto solo lo stato del dispositivo acquisito nel blocco di stato. Qualsiasi altro stato del dispositivo non acquisito con lo stateblock personalizzato non verrà modificato. Anche in questo caso, poiché l'oggetto stateblock è un'interfaccia, è necessario rilasciarlo al termine dell'operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati (Direct3D 9)](states.md)
</dt> </dl>

 

 
