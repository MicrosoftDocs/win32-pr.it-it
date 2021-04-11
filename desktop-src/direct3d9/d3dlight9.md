---
description: Definisce un set di proprietà di illuminazione.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Struttura D3DLIGHT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235073"
---
# <a name="d3dlight9-structure"></a>Struttura D3DLIGHT9

Definisce un set di proprietà di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**

</dd> <dd>

Tipo della sorgente di luce. Questo valore è uno dei membri del tipo enumerato [**D3DLIGHTTYPE**](./d3dlighttype.md) .

</dd> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Colore diffuso emesso dalla luce. Questo membro è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Colore speculare emesso dalla luce. Questo membro è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Di ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Colore di ambiente emesso dalla luce. Questo membro è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) .

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Posizione della luce nello spazio globale, specificata da una struttura [**D3DVECTOR**](d3dvector.md) . Questo membro non ha significato per le luci direzionali e in questo caso viene ignorato.

</dd> <dt>

**Direzione**
</dt> <dd>

Tipo: **[ **D3DVECTOR**](d3dvector.md)**

</dd> <dd>

Direzione della luce che punta allo spazio globale, specificata da una struttura [**D3DVECTOR**](d3dvector.md) . Questo membro ha un significato solo per direzionali e Spotlight. Non è necessario normalizzare questo vettore, ma deve avere una lunghezza diversa da zero.

</dd> <dt>

**Range**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Distanza oltre la quale la luce non ha alcun effetto. Il valore massimo consentito per questo membro è la radice quadrata di FLT \_ max. Questo membro non influisce sulle luci direzionali.

</dd> <dt>

**Falloff**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Diminuisce l'illuminazione tra il cono interno di un punto di Spotlight (l'angolo specificato da Theta) e il bordo esterno del cono esterno (l'angolo specificato da Phi).

L'effetto del decadimento sull'illuminazione è sottile. Inoltre, una lieve riduzione delle prestazioni è dovuta al data shaping della curva di interruzione. Per questi motivi, la maggior parte degli sviluppatori imposta questo valore su 1,0.

</dd> <dt>

**Attenuation0**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore che specifica il modo in cui l'intensità di luce viene modificata rispetto alla distanza. I valori di attenuazione vengono ignorati per le luci direzionali. Questo membro rappresenta una costante di attenuazione. Per informazioni sull'attenuazione, vedere [Proprietà chiare (Direct3D 9)](light-properties.md). I valori validi per questo membro variano da 0,0 a infinito. Per le luci non direzionali, tutti e tre i valori di attenuazione non devono essere impostati su 0,0 nello stesso momento.

</dd> <dt>

**Attenuation1**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore che specifica il modo in cui l'intensità di luce viene modificata rispetto alla distanza. I valori di attenuazione vengono ignorati per le luci direzionali. Questo membro rappresenta una costante di attenuazione. Per informazioni sull'attenuazione, vedere [Proprietà chiare (Direct3D 9)](light-properties.md). I valori validi per questo membro variano da 0,0 a infinito. Per le luci non direzionali, tutti e tre i valori di attenuazione non devono essere impostati su 0,0 nello stesso momento.

</dd> <dt>

**Attenuation2**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valore che specifica il modo in cui l'intensità di luce viene modificata rispetto alla distanza. I valori di attenuazione vengono ignorati per le luci direzionali. Questo membro rappresenta una costante di attenuazione. Per informazioni sull'attenuazione, vedere [Proprietà chiare (Direct3D 9)](light-properties.md). I valori validi per questo membro variano da 0,0 a infinito. Per le luci non direzionali, tutti e tre i valori di attenuazione non devono essere impostati su 0,0 nello stesso momento.

</dd> <dt>

**Theta**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Angolo, in radianti, del cono interno di un Spotlight, ovvero il cono in evidenza completamente illuminato. Questo valore deve essere compreso nell'intervallo compreso tra 0 e il valore specificato da Phi.

</dd> <dt>

**Phi**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Angolo, in radianti, che definisce il bordo esterno del cono esterno del faretto. I punti esterni a questo cono non sono illuminati dal faretto. Questo valore deve essere compreso tra 0 e pi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[**Chiaro**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
