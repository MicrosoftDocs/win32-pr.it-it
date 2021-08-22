---
description: Costanti delle estremità del vertex shader. Queste costanti vengono usate dal membro VS20Caps di D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a199fa5e98040cf100846a4773e1077da04fa43e9d9e77a615017ecb9b32ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988871"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Costanti delle estremità del vertex shader. Queste costanti vengono usate dal membro VS20Caps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)



| \#Definire                              | Valore          | Descrizione                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PREDICATO D3DVS20CAPS \_              | (1 << 0) | Il predicato dell'istruzione è supportato. Vedere [setp \_ comp - e](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH | 24             | Livello massimo di annidamento delle istruzioni di controllo dinamico del flusso ( break[-](../direct3dhlsl/break---vs.md)vs , [break comp - \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH | 0              | Livello minimo di annidamento delle istruzioni di controllo dinamico del flusso ( break[-](../direct3dhlsl/break---vs.md)vs , [break comp - \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ MAX \_ NUMTEMPS                | 32             | Numero massimo di registri temporanei supportati.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MIN \_ NUMTEMPS                | 12             | Numero minimo di registri temporanei supportati.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH  | 4              | Profondità massima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a rep / [e](../direct3dhlsl/rep---vs.md) [call,](../direct3dhlsl/call---vs.md)rispetto a / [callnz bool, rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni .                                                                                           |
| D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH  | 1              | Profondità minima di annidamento del [ciclo ,](../direct3dhlsl/loop---vs.md)rispetto a rep e call, rispetto a / [](../direct3dhlsl/rep---vs.md) [](../direct3dhlsl/call---vs.md) / [callnz bool, rispetto alle](../direct3dhlsl/callnz-bool---vs.md) istruzioni .                                                                                           |



 

## <a name="constant-information"></a>Informazioni sulle costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
