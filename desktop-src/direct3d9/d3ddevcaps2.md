---
description: Flag della funzionalità del driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225626"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Flag della funzionalità del driver D3DDEVCAPS2.



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                                        | Descrizione                                                                                                                                                                                                               |
| \_ADAPTIVETESSRTPATCH D3DDEVCAPS2                | Il dispositivo supporta lo schema a mosaico adattivo delle patch RT                                                                                                                                                                       |
| \_ADAPTIVETESSNPATCH D3DDEVCAPS2                 | Il dispositivo supporta lo schema a mosaico adattivo di N-patch.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ può \_ STRETCHRECT \_ da \_ trame   | Il dispositivo supporta [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando una trama come origine.                                                                                                                       |
| \_DMAPNPATCH D3DDEVCAPS2                         | Il dispositivo supporta le mappe di spostamento per N-patch.                                                                                                                                                                          |
| \_PRESAMPLEDDMAPNPATCH D3DDEVCAPS2               | Il dispositivo supporta le mappe di spostamento precampionate per N-patch. Per ulteriori informazioni sul mapping di spostamento, vedere [mapping di spostamento (Direct3D 9)](displacement-mapping.md).                                           |
| \_STREAMOFFSET D3DDEVCAPS2                       | Il dispositivo supporta gli offset del flusso.                                                                                                                                                                                           |
| \_VERTEXELEMENTSCANSHARESTREAMOFFSET D3DDEVCAPS2 | Più elementi Vertex possono condividere lo stesso offset in un flusso se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo e la dichiarazione del vertice non contiene un elemento con D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
