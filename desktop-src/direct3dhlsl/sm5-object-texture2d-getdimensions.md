---
title: Funzione Texture2D::GetDimensions
description: Restituisce le dimensioni della risorsa. | Funzione Texture2D::GetDimensions
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
ms.openlocfilehash: 46eb5101dc119d2779f60d2e2b39a42c695933a5bffd477b407fea56c930038c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067701"
---
# <a name="texture2dgetdimensions-function"></a>Funzione Texture2D::GetDimensions

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

*MipLevel* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

facoltativo. Livello mipmap (deve essere specificato se *si usa NumberOfLevels).*

</dd> <dt>

*Larghezza* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Larghezza della risorsa, in texel.

</dd> <dt>

*Altezza* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Altezza della risorsa, in texel.

</dd> <dt>

*NumberOfLevels* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Numero di livelli mipmap (richiede *anche MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Questo è un elenco delle versioni di overload di questo metodo.


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



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




