---
description: Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7e5d423169e561df28b5d69017c77a71e183
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998658"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.



| \#Definire                                | Descrizione                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | Il dispositivo può fare luci direzionali.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | Il dispositivo può eseguire il visualizzatore locale.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Quando questo limite è impostato, il dispositivo supporta gli stati del materiale a colori: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS \_ SPECULARMATERIALSOURCE. |
| D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER | Il dispositivo non supporta la generazione di trame in modalità visualizzatore non locale.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | Il dispositivo può eseguire luci posizionali (include punto e punto).                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | Il dispositivo può eseguire texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | Il dispositivo supporta D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| D3DVTXPCAPS \_ TWEENING                   | Il dispositivo può eseguire l'interpolazione dei vertici.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



