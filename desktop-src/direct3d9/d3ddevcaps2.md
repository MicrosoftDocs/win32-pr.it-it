---
description: Flag di funzionalità del driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ef30540f19add130aaca6eb48655a5ac47b2b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999468"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Flag di funzionalità del driver D3DDEVCAPS2.



| \#Definire                                        | Descrizione                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | Il dispositivo supporta lo schema a tessitori adattivi delle patch RT                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | Il dispositivo supporta lo schema a tessitori adattivi di N patch.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ PUÒ ESTENDERE LE \_ \_ \_ TRAME   | Il dispositivo supporta [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando una trama come origine.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | Il dispositivo supporta le mappe di spostamento per le patch N.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | Il dispositivo supporta le mappe di spostamento precampionato per le patch N. Per altre informazioni sul mapping dello spostamento, vedere [Mapping degli spostamenti (Direct3D 9).](displacement-mapping.md)                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | Il dispositivo supporta gli offset di flusso.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Più elementi vertice possono condividere lo stesso offset in un flusso se D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo e la dichiarazione del vertice non ha un elemento \_ con D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
