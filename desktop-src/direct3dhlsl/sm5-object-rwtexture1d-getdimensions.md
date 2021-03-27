---
title: 'Funzione RWTexture1D:: GetDimensions'
description: 'Restituisce le dimensioni della risorsa. | Funzione RWTexture1D:: GetDimensions'
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
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
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981079"
---
# <a name="rwtexture1dgetdimensions-function"></a>Funzione RWTexture1D:: GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Larghezza della risorsa, in Texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Si tratta di un elenco delle versioni di overload di questo metodo.


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
