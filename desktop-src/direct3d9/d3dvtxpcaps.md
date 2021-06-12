---
description: Informazioni su una combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo nella costante D3DVTXPCAPS.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011084"
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



 

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9caps.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



