---
title: Funzione Texture3D::GetDimensions
description: Restituisce le dimensioni della risorsa. | Funzione Texture3D::GetDimensions
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 8a7dd6248b7b6effc08e510ea56da6426c41dc54418bf7ee5da8cdc3c9ad965a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985711"
---
# <a name="texture3dgetdimensions-function"></a>Funzione Texture3D::GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*MipLevel* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

facoltativo. Livello Mipmap (deve essere specificato se *si usa NumberOfLevels).*

</dd> <dt>

*Larghezza* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Larghezza della risorsa, in texel.

</dd> <dt>

*Altezza* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Altezza della risorsa, in texel.

</dd> <dt>

*Profondità* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Profondità delle risorse, in texel.

</dd> <dt>

*NumberOfLevels* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di livelli mipmap (richiede *anche MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Questo è un elenco delle versioni di overload di questo metodo.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
