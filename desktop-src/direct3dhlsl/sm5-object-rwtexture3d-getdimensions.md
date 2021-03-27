---
title: 'Funzione RWTexture3D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture3D:: GetDimensions'
ms.assetid: ba70b955-1e80-4f27-84f1-fc9d26a1f1ab
keywords:
- Funzione GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 499ab493851257030921e9d55f4873eef8726915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352966"
---
# <a name="rwtexture3dgetdimensions-function"></a>Funzione RWTexture3D:: GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Depth
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Larghezza della risorsa, in Texel.

</dd> <dt>

*Altezza* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Altezza della risorsa, in Texel.

</dd> <dt>

*Profondità* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Profondità della risorsa, in Texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Si tratta di un elenco delle versioni di overload di questo metodo.


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
