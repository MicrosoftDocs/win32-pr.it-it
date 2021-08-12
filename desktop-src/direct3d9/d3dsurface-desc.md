---
description: Descrive una superficie.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: D3DSURFACE_DESC struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b18c9cd3428463f82a6e243a57ade3fffd650bb35f2c73234b725fa5bf0607eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300233"
---
# <a name="d3dsurface_desc-structure"></a>Struttura DESC D3DSURFACE \_

Descrive una superficie.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) che descrive il formato della superficie.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DRESOURCETYPE,**](./d3dresourcetype.md) che identifica la risorsa come superficie.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

I valori D3DUSAGE \_ DEPTHSTENCIL o D3DUSAGE \_ RENDERTARGET. Per altre informazioni, vedere [**D3DUSAGE.**](d3dusage.md)

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che specifica la classe di memoria allocata per questa superficie.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DMULTISAMPLE \_ TYPE,**](./d3dmultisample-type.md) che specifica i livelli di multisampling a scena intera supportati dalla superficie.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello di qualità. L'intervallo valido è compreso tra zero e uno minore del livello restituito da pQualityLevels usato da [**CheckDeviceMultiSampleType.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) Il passaggio di un valore più grande restituisce l'errore D3DERR \_ INVALIDCALL. I valori MultisampleQuality delle destinazioni di rendering abbinate, depth stencil superfici e il tipo MultiSample devono corrispondere tutti.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza della superficie, in pixel.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza della superficie, in pixel.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
