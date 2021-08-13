---
description: È anche possibile specificare alfa in un materiale. Per abilitare l'alfa del materiale, impostare lo stato di rendering del materiale diffuso in modo che il runtime usi i componenti di colore con diffusione dei materiali anziché i componenti di colore con diffusione dei vertici.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Alfa materiale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a70ed4a3f5bcaf38f4ace079af5b2e1804af0e24340e5004898c9ed26707d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798978"
---
# <a name="material-alpha-direct3d-9"></a>Alfa materiale (Direct3D 9)

È anche possibile specificare alfa in un materiale. Per abilitare l'alfa del materiale, impostare lo stato di rendering del materiale diffuso in modo che il runtime usi i componenti di colore con diffusione dei materiali anziché i componenti di colore con diffusione dei vertici.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



Inizializzare il materiale con un valore alfa e impostare il materiale prima del disegno.


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 



