---
description: Per determinare se Direct3D supporta l'interpolazione dei vertici, cercare il flag TWEENING D3DVTXPCAPS nel membro \_ VertexProcessingCaps della struttura D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Uso della tween dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14c4d2da3f32698cc24e052a152b674ecb023f79e90541af23374c0903d54d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797089"
---
# <a name="using-vertex-tweening-direct3d-9"></a>Uso della tween dei vertici (Direct3D 9)

Per determinare se Direct3D supporta l'interpolazione dei vertici, cercare il flag TWEENING D3DVTXPCAPS nel membro \_ VertexProcessingCaps della [**struttura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) L'esempio di codice seguente usa il metodo [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) per determinare se la tweening è supportata.


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



Per usare la tween vettoriale, è prima necessario configurare un tipo di vertice personalizzato che usa una seconda posizione normale o una seconda. Nell'esempio di codice seguente viene illustrata una dichiarazione di esempio che include sia un secondo punto che una seconda posizione.


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



Il passaggio successivo consiste nell'impostare la dichiarazione corrente. L'esempio di codice seguente illustra come eseguire questa operazione.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



Per altre informazioni sulla creazione di un tipo di vertice personalizzato e di un vertex buffer, vedere [Creating a Vertex Buffer (Direct3D 9) (Creazione di un vertex buffer (Direct3D 9)](creating-a-vertex-buffer.md)).

> [!Note]  
> Quando l'interpolazione dei vertici è abilitata, nella dichiarazione corrente deve essere presente una seconda posizione o una seconda normale.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tweening vertici](vertex-tweening.md)
</dt> </dl>

 

 
