---
title: 'Funzione Texture2DArray:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture2DArray:: GetDimensions'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981071"
---
# <a name="texture2darraygetdimensions-function"></a>Funzione Texture2DArray:: GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*MipLevel* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

facoltativo. Il livello mipmap (deve essere specificato se si usa *NumberOfLevels* ).

</dd> <dt>

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

*Elementi* \[ di out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Il numero di livelli di mipmap (richiede anche *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Si tratta di un elenco delle versioni di overload di questo metodo.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
