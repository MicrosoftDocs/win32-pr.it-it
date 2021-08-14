---
description: Le applicazioni associano una fase di fusione a ogni trama nel set di trame correnti. Direct3D valuta ogni fase di fusione in ordine, iniziando con la prima trama nel set e terminando con l'ottava.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operazioni e argomenti di fusione tra trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d242092de5919267d30a9b8ff4e7bd2324f0bc3120649d3bb1a423b3462be77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797773"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Operazioni e argomenti di fusione tra trame (Direct3D 9)

Le applicazioni associano una fase di fusione a ogni trama nel set di trame correnti. Direct3D valuta ogni fase di fusione in ordine, iniziando con la prima trama nel set e terminando con l'ottava.

Direct3D applica le informazioni di ogni trama nel set di trame correnti alla fase di fusione associata. Le applicazioni controllano quali informazioni da una fase di trama vengono usate chiamando [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api). È possibile impostare operazioni separate per i canali di colore e alfa e ogni operazione usa due argomenti. Specificare le operazioni del canale colore usando lo stato della fase COLOROP D3DTSS; specificare le operazioni alfa usando \_ D3DTSS \_ ALPHAOP. Entrambi gli stati di fase usano valori del [**tipo enumerato D3DTEXTUREOP.**](./d3dtextureop.md)

Gli argomenti di fusione trame usano i membri D3DTSS \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 e D3DTSS ALPHARG2 del tipo \_ [**enumerato D3DTEXTURESTAGESTATETYPE.**](./d3dtexturestagestatetype.md) I valori degli argomenti corrispondenti vengono identificati tramite [D3DTA.](d3dta.md)

> [!Note]  
> È possibile disabilitare una fase di trama e tutte le fasi di fusione della trama successive nella cascata impostando l'operazione di colore per tale fase su D3DTOP \_ DISABLE. La disabilitazione dell'operazione di colore disabilita in modo efficace anche l'operazione alfa. Le operazioni alfa non possono essere disabilitate quando sono abilitate le operazioni sui colori. L'impostazione dell'operazione alfa su D3DTOP DISABLE quando è abilitata la \_ fusione dei colori causa un comportamento non definito.

 

Per determinare le operazioni di fusione trame supportate di un dispositivo, eseguire una query sul membro TextureCaps della [**struttura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione tra trame](texture-blending.md)
</dt> </dl>

 

 
