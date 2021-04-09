---
description: Un blocco di stato è un gruppo di Stati del dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965462"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>Stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)

Un blocco di stato è un gruppo di Stati del dispositivo. Lo stato del dispositivo è costituito dallo stato di rendering, dallo stato del vertice, dallo stato dei pixel o da tutti i precedenti. Un blocco di stato contiene uno snapshot dello stato corrente di un dispositivo oppure è possibile creare un blocco di stato che registra ogni modifica dello stato apportata dall'applicazione.

## <a name="capture-a-block-of-state"></a>Acquisisci un blocco di stato

Scegliere il tipo di stato che si desidera acquisire e creare un blocco di stato simile al seguente:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) crea un blocco di stato e acquisisce automaticamente lo stato del dispositivo. Lo stato del dispositivo viene specificato dal tipo di blocco di stato nel primo argomento. Questo stato può essere uno dei seguenti: tutti gli Stati del dispositivo (vedere [salvare tutti gli Stati dei dispositivi con StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), tutti i pixel (vedere [salvataggio dello stato dei pixel con StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) o tutto lo stato del vertice (vedere [salvataggio degli Stati dei vertici con un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

Il sistema degli effetti usa un blocco di stato per salvare lo stato. Dopo la chiamata di [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) , viene creato un blocco di stato e viene acquisito lo stato. Quando viene chiamato [**ID3DXEffect:: end**](id3dxeffect--end.md) , lo stato del blocco di stato viene riapplicato al dispositivo.

## <a name="capture-individual-states"></a>Acquisisci singoli Stati

Per salvare una sequenza di stato personalizzata, eseguire il wrapping dello stato che si desidera salvare in una coppia [**IDirect3DDevice9:: BeginStateBlock**](/windows/desktop/api) e [**IDirect3DDevice9:: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) . BeginStateBlock indica al dispositivo corrente di impostare un blocco di stato e aggiungervi tutte le modifiche di stato che si verificano fino a quando non viene chiamato EndStateBlock. Ecco un esempio:


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



In questo modo si salva un numero qualsiasi di modifiche di stato in qualsiasi sequenza in un stateblock personalizzato. In seguito, quando si vuole usare stateblock per reimpostare lo stato del dispositivo, chiamare [**IDirect3DStateBlock9:: Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Questa operazione sovrascriverà solo lo stato del dispositivo acquisito nel blocco di stato. Qualsiasi altro stato del dispositivo che non è stato acquisito con il stateblock personalizzato non verrà modificato. Ancora una volta, poiché l'oggetto stateblock è un'interfaccia, sarà necessario rilasciarlo al termine dell'operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati (Direct3D 9)](states.md)
</dt> </dl>

 

 
