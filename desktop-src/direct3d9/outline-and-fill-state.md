---
description: Viene eseguito il rendering delle primitive senza trame con il colore specificato dal materiale o con i colori specificati per i vertici, se presenti.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Stato di riempimento e contorno (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303800"
---
# <a name="outline-and-fill-state-direct3d-9"></a>Stato di riempimento e contorno (Direct3D 9)

Viene eseguito il rendering delle primitive senza trame con il colore specificato dal materiale o con i colori specificati per i vertici, se presenti. È possibile selezionare il metodo per riempirli specificando un valore definito dal tipo enumerato [**D3DFILLMODE**](./d3dfillmode.md) per lo stato di \_ rendering D3DRS FillMode.

Per abilitare la rethering, l'applicazione deve passare il \_ valore enumerato D3DRS DITHERENABLE come primo parametro a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate). Deve impostare il secondo parametro su **true** per abilitare la dithering e **false** per disabilitarlo.

In alcuni casi, il disegno dell'ultimo pixel in una riga può causare una sovrapposizione approfondita con le primitive circostanti. È possibile controllare questa operazione usando il \_ valore enumerato di D3DRS LASTPIXEL. Tuttavia, non modificare questa impostazione senza alcuna premeditazione. In alcune condizioni, la disattivazione del rendering dell'ultimo pixel può causare Gap non visivi tra primitive.

È possibile disegnare le strutture degli oggetti impostando il modello di disegno a linee appropriato. Lo stato predefinito di disegno della linea consiste nel disegnare linee continue. Per altre informazioni, vedere [supporto per la creazione di linee nello stato di rendering D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
