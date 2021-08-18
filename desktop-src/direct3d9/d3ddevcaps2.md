---
description: Flag di funzionalità del driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d08dfe7e321fc9aa0d4d91bea49be2c96c02b8a2aca25045a180c16c2364
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728601"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Flag di funzionalità del driver D3DDEVCAPS2.



| \#Definire                                        | Descrizione                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | Il dispositivo supporta la tessellazione adattiva delle patch RT                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | Il dispositivo supporta la tessellazione adattiva delle N patch.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ PUÒ \_ ESTENDERSI DALLE \_ \_ TRAME   | Il dispositivo supporta [**StretchRect usando**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) una trama come origine.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | Il dispositivo supporta le mappe di spostamento per le patch N.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | Il dispositivo supporta mappe di spostamento precampionato per N-patch. Per altre informazioni sul mapping dello spostamento, vedere [Mapping di spostamento (Direct3D 9).](displacement-mapping.md)                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | Il dispositivo supporta gli offset di flusso.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Più elementi vertice possono condividere lo stesso offset in un flusso se D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo e la dichiarazione del vertice non ha un elemento \_ con D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
