---
description: Le applicazioni associano una fase di fusione a ogni trama nel set di trame correnti. Direct3D valuta ogni fase di fusione in ordine, iniziando dalla prima trama del set e terminando con l'ottavo.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operazioni di combinazione di trame e argomenti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304192"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Operazioni di combinazione di trame e argomenti (Direct3D 9)

Le applicazioni associano una fase di fusione a ogni trama nel set di trame correnti. Direct3D valuta ogni fase di fusione in ordine, iniziando dalla prima trama del set e terminando con l'ottavo.

Direct3D applica le informazioni di ogni trama nel set di trame correnti alla fase di fusione a essa associata. Le applicazioni controllano quali informazioni di una fase della trama vengono utilizzate chiamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api). È possibile impostare operazioni separate per i canali colore e alfa e ogni operazione utilizza due argomenti. Specificare le operazioni del canale colori utilizzando lo \_ stato della fase COLOROP di D3DTSS. specificare le operazioni alfa utilizzando D3DTSS \_ ALPHAOP. Entrambi gli Stati della fase utilizzano valori del tipo enumerato [**D3DTEXTUREOP**](./d3dtextureop.md) .

Gli argomenti di combinazione di trame utilizzano i \_ membri D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 e D3DTSS \_ ALPHARG2 del tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . I valori degli argomenti corrispondenti vengono identificati utilizzando [D3DTA](d3dta.md).

> [!Note]  
> È possibile disabilitare una fase di trama e tutte le fasi successive di combinazione di trame in Cascade, impostando l'operazione relativa al colore per la fase su D3DTOP \_ Disable. La disabilitazione dell'operazione di colore disattiva efficacemente anche l'operazione Alpha. Non è possibile disabilitare le operazioni Alpha quando sono abilitate le operazioni sui colori. L'impostazione dell'operazione Alpha su D3DTOP \_ Disabilita quando è abilitata la fusione dei colori causa un comportamento non definito.

 

Per determinare le operazioni di blending di trama supportate di un dispositivo, eseguire una query sul membro TextureCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazione di trame](texture-blending.md)
</dt> </dl>

 

 
