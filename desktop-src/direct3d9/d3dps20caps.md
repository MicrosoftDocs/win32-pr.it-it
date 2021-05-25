---
description: Flag di funzionalità pixel shader.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eed8fb6c7a5c4c4da31185dc4cc8c1661f7109
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343116"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Flag di funzionalità pixel shader.



| \#Definire                                     | Valore          | Descrizione                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Lo swizzling arbitrario è supportato.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Sono supportate le istruzioni per la sfumatura.                                                                                                                                                                              |
| PREDICAZIONE D3DD3DPSHADERCAPS2 \_ 0 \_           | (1 << 2) | La predicazione dell'istruzione è supportata. Vedere [setp \_ comp - ps](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | Non esiste alcun limite al numero di operazioni di lettura dipendenti per ogni istruzione.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | Non esiste alcun limite al numero di istruzioni tex.                                                                                                                                                              |
| D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH        | 24             | Livello massimo di annidamento delle istruzioni di controllo dinamico del flusso (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH        | 0              | Livello minimo di annidamento delle istruzioni di controllo dinamico del flusso (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MAX \_ NUMTEMPS                       | 32             | Il driver supporterà al massimo questo numero di registri temporanei.                                                                                                                                                     |
| D3DPS20 \_ MIN \_ NUMTEMPS                       | 12             | Il driver supporterà almeno questo numero di registri temporanei.                                                                                                                                                    |
| D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH         | 4              | Profondità massima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a rep / [e](../direct3dhlsl/rep---vs.md) [call,](../direct3dhlsl/call---vs.md)rispetto a / [callnz bool, rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni . |
| D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH         | 1              | Profondità minima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a rep e call, rispetto a / [](../direct3dhlsl/rep---vs.md) [](../direct3dhlsl/call---vs.md) / [callnz bool, rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni . |
| D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS            | 512            | Il driver supporterà al massimo queste numerose istruzioni.                                                                                                                                                           |
| D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS            | 96             | Il driver supporterà almeno queste numerose istruzioni.                                                                                                                                                          |



 

Queste costanti vengono usate dal membro D3DPSHADERCAPS2 \_ 0 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informazioni sulle costanti



|  Requisito                        | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
