---
title: 'Funzione Texture2D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione Texture2D:: GetDimensions'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995629"
---
# <a name="texture2dgetdimensions-function"></a>Funzione Texture2D:: GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*MipLevel* \[ in\]
</dt> <dd>

Tipo: **uint**

facoltativo. Il livello mipmap (deve essere specificato se si usa *NumberOfLevels* ).

</dd> <dt>

*Larghezza* \[ out\]
</dt> <dd>

Tipo: **uint**

Larghezza della risorsa, in Texel.

</dd> <dt>

*Altezza* \[ out\]
</dt> <dd>

Tipo: **uint**

Altezza della risorsa, in Texel.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **uint**

Il numero di livelli di mipmap (richiede anche *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Si tratta di un elenco delle versioni di overload di questo metodo.


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




