---
description: Un blocco di stato può essere usato per acquisire tutti gli Stati dei dispositivi. vedere lo stato di salvataggio e ripristino dei blocchi di stato (Direct3D 9).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Salvataggio di tutti gli Stati dei dispositivi con StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304194"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Salvataggio di tutti gli Stati dei dispositivi con StateBlock (Direct3D 9)

Un blocco di stato può essere usato per acquisire tutti gli Stati dei dispositivi. vedere lo [stato di salvataggio e ripristino dei blocchi di stato (Direct3D 9)](state-blocks-save-and-restore-state.md). Gli elementi di stato seguenti sono inclusi nello stato del dispositivo:

-   Stato vertice (vedere [salvataggio degli Stati dei vertici con StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Stato dei pixel (vedere [salvataggio dello stato dei pixel con StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Ogni trama assegnata a un campionatore.
-   Ogni trama del vertice.
-   Trama della mappa di spostamento.
-   Tavolozza di trama corrente.
-   Per ogni flusso di vertici: un puntatore al buffer dei vertici, ogni argomento di [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api)e il divisore, se presente, da [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Puntatore al buffer dell'indice.
-   Viewport.
-   Rettangolo a forbice.
-   Matrici internazionali, di visualizzazione e di proiezione.
-   Trasformazioni della trama.
-   Eventuali piani di ritaglio.
-   Materiale corrente.

Per acquisire tutti gli Stati del dispositivo con un blocco di stato, specificare D3DSBT \_ all durante la chiamata a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stato di salvataggio e ripristino del blocco di stato](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
