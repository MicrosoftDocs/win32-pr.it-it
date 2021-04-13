---
description: Specifica le proprietà del materiale.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Struttura D3DMATERIAL9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401977"
---
# <a name="d3dmaterial9-structure"></a>Struttura D3DMATERIAL9

Specifica le proprietà del materiale.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>Members

<dl> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valore che specifica il colore diffuso del materiale. Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Di ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valore che specifica il colore di ambiente del materiale. Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valore che specifica il colore speculare del materiale. Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Emissiva**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valore che specifica il colore emissivo del materiale. Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Potere**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore a virgola mobile che specifica l'intensità delle evidenziazioni speculari. Maggiore è il valore, più nitida è l'evidenziazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per disattivare le evidenziazioni speculari, impostare D3DRS \_ SPECULARENABLE su **false** usando [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Questa è l'opzione più rapida perché non verrà calcolata alcuna evidenziazione speculare.

Per ulteriori informazioni sull'utilizzo del motore di illuminazione per calcolare l'illuminazione speculare, vedere [illuminazione speculare (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9:: getmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
