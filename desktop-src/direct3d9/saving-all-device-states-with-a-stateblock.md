---
description: Un blocco di stato può essere usato per acquisire tutti gli stati del dispositivo (vedere State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Salvataggio di tutti gli stati del dispositivo con stateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffda5b5d637a31c774e97af85ddeca78b0995ee53c015bb2dcd245b42277a4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520082"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Salvataggio di tutti gli stati del dispositivo con stateBlock (Direct3D 9)

Un blocco di stato può essere usato per acquisire tutti gli stati del dispositivo (vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)). Nello stato del dispositivo sono inclusi gli elementi di stato seguenti:

-   Stato del vertice (vedere [Salvataggio degli stati dei vertici con uno StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Stato pixel (vedere [Salvataggio dello stato dei pixel con stateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Ogni trama assegnata a un campionatore.
-   Ogni trama vertice.
-   Ogni trama della mappa di spostamento.
-   Tavolozza di trame corrente.
-   Per ogni flusso di vertici: un puntatore al vertex buffer, ogni argomento di [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api)e il divisore (se presente) da [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Puntatore al index buffer.
-   Riquadro di visualizzazione.
-   Rettangolo delle forbici.
-   Matrici di mondo, visualizzazione e proiezione.
-   La trama viene trasformata.
-   Piani di ritaglio (se presenti).
-   Materiale corrente.

Per acquisire tutti gli stati del dispositivo con un blocco di stato, specificare D3DSBT ALL quando si \_ chiama [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[State Blocks Save and Restore State](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
