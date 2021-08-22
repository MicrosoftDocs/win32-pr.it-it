---
title: Come creare una trama
description: Questo argomento illustra come creare una trama.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6539caec121f301dd89906f7cd78134d3b7cd79083c0d185af63d488ef1648eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565551"
---
# <a name="how-to-create-a-texture"></a>Procedura: Creare una trama

Il modo più semplice per creare una trama consiste nel descrivere le proprietà e chiamare l'API di creazione della trama. Questo argomento illustra come creare una trama.

**Per creare una trama**

1.  Compilare una [**struttura D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) con una descrizione dei parametri di trama.
2.  Creare la trama chiamando [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) con la descrizione della trama.

In questo esempio viene creata una trama 256 x 256, con utilizzo [**dinamico,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)da usare come risorsa [**shader**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) con accesso [**in scrittura della cpu.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)


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

 

 




