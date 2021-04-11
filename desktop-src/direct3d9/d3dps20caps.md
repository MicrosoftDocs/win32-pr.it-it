---
description: Flag di funzionalità pixel shader.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127534"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Flag di funzionalità pixel shader.



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                                     | Valore          | Descrizione                                                                                                                                                                                                       |
| \_ARBITRARYSWIZZLE D3DD3DPSHADERCAPS2 0 \_      | (1 << 0) | Il swizzling arbitrario è supportato.                                                                                                                                                                                 |
| \_GRADIENTINSTRUCTIONS D3DD3DPSHADERCAPS2 0 \_  | (1 << 1) | Sono supportate le istruzioni per la sfumatura.                                                                                                                                                                              |
| \_Predicazione D3DD3DPSHADERCAPS2 0 \_           | (1 << 2) | L'istruzione predicazione è supportata. Vedere [setp \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| \_NODEPENDENTREADLIMIT D3DD3DPSHADERCAPS2 0 \_  | (1 << 3) | Non esiste alcun limite al numero di letture dipendenti per istruzione.                                                                                                                                               |
| \_NOTEXINSTRUCTIONLIMIT D3DD3DPSHADERCAPS2 0 \_ | (1 << 4) | Non esiste alcun limite al numero di istruzioni Tex.                                                                                                                                                              |
| D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH        | 24             | Il livello massimo di nidificazione delle istruzioni di controllo del flusso dinamico (Break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH        | 0              | Il livello minimo di nidificazione delle istruzioni di controllo del flusso dinamico (Break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Max \_ NUMTEMPS                       | 32             | Il driver supporterà al massimo questo numero di registri temporanei.                                                                                                                                                     |
| D3DPS20 \_ Min \_ NUMTEMPS                       | 12             | Il driver supporterà almeno questo numero di registri temporanei.                                                                                                                                                    |
| D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH         | 4              | Profondità massima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) . |
| D3DPS20 \_ Min \_ STATICFLOWCONTROLDEPTH         | 1              | Profondità minima di annidamento delle istruzioni [loop-vs](../direct3dhlsl/loop---vs.md) / [Rep-vs](../direct3dhlsl/rep---vs.md) e [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) . |
| D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS            | 512            | Il driver supporterà al massimo questo numero di istruzioni.                                                                                                                                                           |
| D3DPS20 \_ Min \_ NUMINSTRUCTIONSLOTS            | 96             | Il driver supporterà almeno questo numero di istruzioni.                                                                                                                                                          |



 

Queste costanti vengono usate dal \_ membro D3DPSHADERCAPS2 0 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
