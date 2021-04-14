---
description: Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401502"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                                | Descrizione                                                                                                                                                                                        |
| \_DIRECTIONALLIGHTS D3DVTXPCAPS          | Il dispositivo può eseguire luci direzionali.                                                                                                                                                                  |
| \_LOCALVIEWER D3DVTXPCAPS                | Il dispositivo può eseguire il visualizzatore locale.                                                                                                                                                                        |
| \_MATERIALSOURCE7 D3DVTXPCAPS            | Quando questo limite è impostato, il dispositivo supporta gli Stati del materiale colore: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS SPECULARMATERIALSOURCE \_ . |
| D3DVTXPCAPS \_ No \_ TEXGEN \_ NONLOCALVIEWER | Il dispositivo non supporta la generazione di trama in modalità visualizzatore non locale.                                                                                                                               |
| \_POSITIONALLIGHTS D3DVTXPCAPS           | Il dispositivo può eseguire luci posizionali (include punto e punto).                                                                                                                                         |
| \_TEXGEN D3DVTXPCAPS                     | Il dispositivo può eseguire texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | Il dispositivo supporta D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| \_Interpolazione D3DVTXPCAPS                   | Il dispositivo può eseguire l'interpolazione dei vertici.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3d9caps. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



