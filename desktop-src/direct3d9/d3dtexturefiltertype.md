---
description: Definisce le modalità di filtro trame per una fase di trama.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumerazione D3DTEXTUREFILTERTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343006"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Enumerazione D3DTEXTUREFILTERTYPE

Definisce le modalità di filtro trame per una fase di trama.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**
</dt> <dd>

Se usato con [**D3DSAMP \_ MIPFILTER,**](./d3dsamplerstatetype.md)disabilita l'applicazione mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**PUNTO D3DTEXF \_**
</dt> <dd>

Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)specifica che il filtro dei punti deve essere usato rispettivamente come filtro di ingrandimento o minificazione della trama. Se usato con **D3DSAMP \_ MIPFILTER,** abilita l'applicazione mipmapping e specifica che il rasterizzatore sceglie il colore dal texel del livello mip più vicino.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**LINEARE D3DTEXF \_**
</dt> <dd>

Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)specifica che il filtro lineare deve essere usato rispettivamente come filtro di ingrandimento o minificazione della trama. Se usato con **D3DSAMP \_ MIPFILTER,** abilita l'applicazione mipmapping e il filtro trilineare. Specifica che il rasterizzatore interpola tra i due livelli mip più vicini.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROP**
</dt> <dd>

Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)specifica che il filtro trame anisotropo usato rispettivamente come filtro di ingrandimento o minificazione della trama. Compensa la distorsione causata dalla differenza di angolo tra il poligono della trama e il piano dello schermo. **L'uso con D3DSAMP \_ MIPFILTER** non è definito.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Filtro a tent di 4 campioni usato come filtro di ingrandimento o minificazione della trama. [**L'uso con D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

Filtro Gaussiano a 4 campioni usato come filtro di ingrandimento o minimicazione della trama. [**L'uso con D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

Filtro di convoluzione per trame monocroma. Vedere [D3DFMT \_ A1.](d3dformat.md)

Differenze tra Direct3D 9 e Direct3D 9Ex:

- Questo flag è disponibile solo in Direct3D 9Ex.



 

[**L'uso con D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DTEXTUREFILTERTYPE viene usato da [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) insieme [**a D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) per definire le modalità di filtro della trama per una fase della trama.

Per verificare se un formato supporta tipi di filtro di trama diversi da D3DTEXF POINT (che è sempre supportato), chiamare \_ [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ FILTER.

Impostare il filtro di ingrandimento di una fase della trama chiamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il valore D3DSAMP MAGFILTER come secondo parametro e un membro di questa enumerazione come terzo \_ parametro.

Impostare il filtro di minificazione di una fase della trama chiamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il valore D3DSAMP MINFILTER come secondo parametro e un membro di questa enumerazione come terzo \_ parametro.

Impostare il filtro di trama per l'uso tra livelli mipmap chiamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il valore MIPFILTER D3DSAMP come secondo parametro e un membro di questa enumerazione come terzo \_ parametro.

Non tutte le modalità di filtro valide per un dispositivo verranno applicate alle mappe di volume. In generale, i filtri di ingrandimento D3DTEXF POINT e \_ D3DTEXF \_ LINEAR saranno supportati per le mappe di volume. Se si imposta D3DPTEXTURECAPS \_ MIPVOLUMEMAP, i filtri mipmap D3DTEXF POINT e \_ D3DTEXF POINT e \_ D3DTEXF LINEAR saranno supportati per le mappe \_ di volume. Il dispositivo può supportare o meno il filtro mipmap D3DTEXF \_ LINEAR per le mappe dei volumi. I dispositivi che supportano il filtro anisotropo per le mappe 2D non supportano necessariamente il filtro anisotropo per le mappe di volume. Tuttavia, le applicazioni che abilitano il filtro anisotropo riceveranno il filtro migliore disponibile (probabilmente lineare) se il filtro anisotropo non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
