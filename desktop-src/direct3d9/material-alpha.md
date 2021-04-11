---
description: È anche possibile specificare Alpha in un materiale. Per abilitare il materiale Alfa, impostare lo stato di rendering del materiale diffuso in modo che il runtime utilizzerà i componenti dei colori a diffusione del materiale anziché i componenti dei colori con diffusione del vertice.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Materiale Alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123339"
---
# <a name="material-alpha-direct3d-9"></a>Materiale Alfa (Direct3D 9)

È anche possibile specificare Alpha in un materiale. Per abilitare il materiale Alfa, impostare lo stato di rendering del materiale diffuso in modo che il runtime utilizzerà i componenti dei colori a diffusione del materiale anziché i componenti dei colori con diffusione del vertice.


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

 

 



