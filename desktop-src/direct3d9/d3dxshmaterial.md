---
description: Caratteristiche del materiale PRT (pre-Computed Radiance Transfer) di sfericità (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Struttura D3DXSHMATERIAL (D3dx9mesh. h)
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
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322592"
---
# <a name="d3dxshmaterial-structure"></a>Struttura D3DXSHMATERIAL

Caratteristiche del materiale PRT (pre-Computed Radiance Transfer) di sfericità (SH).

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

Diffonde l'albedo della superficie. Questo valore viene ignorato se l'oggetto è un mirror.

</dd> <dt>

**bMirror**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Deve essere impostato su **false**.

</dd> <dt>

**bSubSurf**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Impostare su **true** per abilitare la dispersione della sottosuperficie; qualsiasi oggetto che esegue la dispersione della sottosuperficie non può essere un mirror.

</dd> <dt>

**RelativeIndexOfRefraction**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

L'indice relativo della rifrazione è il rapporto tra due indici assoluti di rifrazione. Un indice di rifrazione è il rapporto tra il seno dell'angolo di incidenza e il seno dell'angolo di rifrazione.

</dd> <dt>

**Assorbimento**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Il coefficiente di assorbimento è un parametro dell'equazione di rendering del volume utilizzato per modellare la propagazione leggera in un supporto partecipante.

</dd> <dt>

**ReducedScattering**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Il coefficiente di dispersione ridotto è un parametro per l'equazione di rendering del volume utilizzato per modellare la propagazione leggera in un supporto partecipante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le scene non spettrali usano il canale rosso dai materiali anziché il valore della luminanza.

Per ulteriori informazioni su PRT, vedere:

-   Procedura di Jensen, Henrik Wann, et al. Siggraph: modello pratico per il trasporto leggero della sottosuperficie, 2001.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
