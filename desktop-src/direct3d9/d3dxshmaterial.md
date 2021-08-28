---
description: Caratteristiche del materiale Spherical armoniche (SH) precomputed radiance transfer (PRT).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Struttura D3DXSHMATERIAL (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 4bfbf00c7d8654ad851ca8c691c9f028c09648219dbe76bb4ef07fe3b830e4d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849721"
---
# <a name="d3dxshmaterial-structure"></a>Struttura D3DXSHMATERIAL

Caratteristiche del materiale Spherical armoniche (SH) precomputed radiance transfer (PRT).

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a>Members

<dl> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Albedo diffuso della superficie. Questo valore viene ignorato se l'oggetto è un mirror.

</dd> <dt>

**bMirror**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Deve essere impostato su **FALSE.**

</dd> <dt>

**bSubSurf**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Impostare su **TRUE per** abilitare la dispersione sottosurface; qualsiasi oggetto che esegue la dispersione sottosurface non può essere un mirror.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

L'indice relativo della rifrazione è il rapporto tra due indici assoluti di rifrazione. Un indice di rifrazione è il rapporto tra il seno dell'angolo di incidenza e il seno dell'angolo di rifrazione.

</dd> <dt>

**Assorbimento**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Il coefficiente di assorbimento è un parametro dell'equazione di rendering del volume usata per modellare la propagazione della luce in un supporto partecipante.

</dd> <dt>

**Riduzione della scalabilità**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Il coefficiente di dispersione ridotto è un parametro dell'equazione di rendering del volume usata per modellare la propagazione della luce in un supporto partecipante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le scene non spettrale usano il canale rosso dei materiali anziché il valore di luminance.

Per altre informazioni su PRT, vedere:

-   Jensen, Enrichk Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
