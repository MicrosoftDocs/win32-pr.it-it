---
description: Definisce le modalità di filtro della trama per una fase della trama.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumerazione D3DTEXTUREFILTERTYPE (D3D9Types. h)
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
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322306"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Enumerazione D3DTEXTUREFILTERTYPE

Definisce le modalità di filtro della trama per una fase della trama.

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

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ None**
</dt> <dd>

Se usato con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), Disabilita mapping MIP.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**Punto di D3DTEXF \_**
</dt> <dd>

Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), specifica che il filtro punti deve essere usato rispettivamente come ingrandimento della trama o filtro minification. Se usato con **D3DSAMP \_ MIPFILTER**, Abilita mapping MIP e specifica che il rasterizzatore sceglie il colore dal Texel del livello MIP più vicino.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ lineare**
</dt> <dd>

Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), specifica che è necessario usare il filtro lineare come ingrandimento della trama o filtro minification rispettivamente. Se usato con **D3DSAMP \_ MIPFILTER**, Abilita il filtro mapping MIP e trilineare; specifica che l'rasterizzazione Interpola tra i due livelli MIP più vicini.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotropico**
</dt> <dd>

Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), specifica che il filtro di trama anisotropico viene usato rispettivamente come ingrandimento della trama o filtro minification. Compensa la distorsione causata dalla differenza nell'angolo tra il poligono di trama e il piano dello schermo. L'uso di con **D3DSAMP \_ MIPFILTER** non è definito.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**\_PYRAMIDALQUAD D3DTEXF**
</dt> <dd>

Un filtro tenda da 4 campioni usato come ingrandimento della trama o filtro minification. L'uso di con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**\_GAUSSIANQUAD D3DTEXF**
</dt> <dd>

Un filtro di controllo gaussiana di 4 campioni usato come ingrandimento della trama o filtro minification. L'uso di con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**\_CONVOLUTIONMONO D3DTEXF**
</dt> <dd>

Filtro di convoluzione per le trame monocromatiche. Vedere [D3DFMT \_ a1](d3dformat.md).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/> |



 

L'uso di con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DTEXTUREFILTERTYPE viene usato da [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) insieme a [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) per definire le modalità di filtro della trama per una fase della trama.

Per verificare se un formato supporta tipi di filtro di trama diversi dal punto di D3DTEXF \_ (che è sempre supportato), chiamare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con il \_ filtro query D3DUSAGE \_ .

Impostare il filtro di ingrandimento di una fase trama chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il \_ valore D3DSAMP MAGFILTER come secondo parametro e un membro di questa enumerazione come terzo parametro.

Impostare il filtro minification della fase della trama chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il \_ valore D3DSAMP MINFILTER come secondo parametro e un membro di questa enumerazione come terzo parametro.

Impostare il filtro di trama per usare i livelli between-mipmap chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il \_ valore D3DSAMP MIPFILTER come secondo parametro e un membro di questa enumerazione come terzo parametro.

Non tutte le modalità di filtro valide per un dispositivo verranno applicate alle mappe del volume. In generale, \_ \_ i filtri di ingrandimento lineari D3DTEXF Point e D3DTEXF sono supportati per le mappe dei volumi. Se \_ è impostato D3DPTEXTURECAPS MIPVOLUMEMAP, i filtri D3DTEXF \_ Point mipmap Filter e D3DTEXF \_ Point e D3DTEXF \_ Linear minification saranno supportati per le mappe del volume. Il dispositivo può supportare o meno il filtro D3DTEXF \_ lineare mipmap per mappe del volume. I dispositivi che supportano il filtro anisotropico per le mappe 2D non supportano necessariamente il filtro anisotropico per le mappe del volume. Tuttavia, le applicazioni che abilitano il filtro anisotropico riceveranno il migliore filtro disponibile (probabilmente lineare) se il filtro anisotropico non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



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

[**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
