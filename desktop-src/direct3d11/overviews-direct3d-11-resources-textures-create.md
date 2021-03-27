---
title: Come creare una trama
description: In questo argomento viene illustrato come creare una trama.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d3c4715bb4c790ea772dcbba4834051946747e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712058"
---
# <a name="how-to-create-a-texture"></a>Procedura: creare una trama

Il modo più semplice per creare una trama consiste nel descrivere le proprietà e chiamare l'API per la creazione di trame. In questo argomento viene illustrato come creare una trama.

**Per creare una trama**

1.  Compilare una struttura [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) con una descrizione dei parametri della trama.
2.  Creare la trama chiamando [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) con la descrizione della trama.

Questo esempio crea una trama 256 x 256, con [**utilizzo dinamico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), da usare come [**risorsa shader**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) con accesso in [**scrittura alla CPU**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




