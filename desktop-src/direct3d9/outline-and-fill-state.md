---
description: Il rendering delle primitive senza trame viene eseguito con il colore specificato dal materiale o con i colori specificati per i vertici, se presenti.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Stato contorno e riempimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db18c38b7511d6fd7954ffdbf18b9e5681cb884414373fd7a22dba2ade3bebf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068941"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Stato contorno e riempimento (Direct3D 9)

Il rendering delle primitive senza trame viene eseguito con il colore specificato dal materiale o con i colori specificati per i vertici, se presenti. È possibile selezionare il metodo per riempirli specificando un valore definito dal tipo enumerato [**D3DFILLMODE**](./d3dfillmode.md) per lo stato di \_ rendering FILLMODE D3DRS.

Per abilitare il dithering, l'applicazione deve passare il valore enumerato D3DRS DITHERENABLE come primo parametro \_ a [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate). È necessario impostare il secondo parametro su **TRUE per** abilitare il dithering e **FALSE** per disabilitarlo.

A volte, il disegno dell'ultimo pixel in una linea può causare una sovrapposizione antiestetriva con le primitive circostanti. È possibile controllare questo valore usando il valore enumerato \_ LASTPIXEL D3DRS. Tuttavia, non modificare questa impostazione senza un certo preavviso. In alcune condizioni, l'eliminazione del rendering dell'ultimo pixel può causare lacune poco erre tra le primitive.

I contorni degli oggetti possono essere disegnati impostando il modello di disegno a linee appropriato. Lo stato di disegno linea predefinito è disegnare linee solide. Per altre informazioni, vedere Supporto del disegno linea nello stato di rendering [D3DX (Direct3D 9).](line-drawing-support-in-d3dx.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
