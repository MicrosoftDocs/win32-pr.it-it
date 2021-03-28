---
title: 'Funzione Texture1D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture1D:: GetDimensions'
ms.assetid: eb8fc02f-01c8-44b9-9d7e-faf59660c287
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
ms.openlocfilehash: fdd9b79a1cc1fa2a5a8db3e0db7a7163878b066b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530708"
---
# <a name="texture1dgetdimensions-function"></a>Funzione Texture1D:: GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*MipLevel* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

facoltativo. Livello mipmap (deve essere specificato se viene usato *NumberOfLevels* ).

</dd> <dt>

*Larghezza* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Larghezza della risorsa, in Texel.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Il numero di livelli di mipmap (richiede anche *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Si tratta di un elenco delle versioni di overload di questo metodo.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float NumberOfLevels);

void GetDimensions(out float Width);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
