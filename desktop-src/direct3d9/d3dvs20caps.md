---
description: Costanti caps del vertex shader. Queste costanti vengono usate dal membro VS20Caps di D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304992"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Costanti caps del vertex shader. Queste costanti vengono usate dal membro VS20Caps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).



| \#definire                              | Valore          | Descrizione                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Predicazione D3DVS20CAPS              | (1 << 0) | L'istruzione predicazione è supportata. Vedere [setp \_ comp-vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH | 24             | Il livello massimo di nidificazione delle istruzioni per il controllo dinamico del flusso ([Break-vs](../direct3dhlsl/break---vs.md), [break \_ comp-vs](../direct3dhlsl/break-comp---vs.md), [Breakp-](../direct3dhlsl/breakp---vs.md)vs, [if \_ comp-vs](../direct3dhlsl/if-comp---vs.md), if comp \_ -vs, se [predazione](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH | 0              | Il livello minimo di nidificazione delle istruzioni per il controllo dinamico del flusso ([Break-vs](../direct3dhlsl/break---vs.md), [break \_ comp-vs](../direct3dhlsl/break-comp---vs.md), [Breakp-](../direct3dhlsl/breakp---vs.md)vs, [if \_ comp-vs](../direct3dhlsl/if-comp---vs.md), if comp \_ -vs, se [predazione](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Max \_ NUMTEMPS                | 32             | Numero massimo di registri temporanei supportati.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Min \_ NUMTEMPS                | 12             | Numero minimo di registri temporanei supportati.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH  | 4              | Profondità massima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .                                                                                           |
| D3DVS20 \_ Min \_ STATICFLOWCONTROLDEPTH  | 1              | Profondità minima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .                                                                                           |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
