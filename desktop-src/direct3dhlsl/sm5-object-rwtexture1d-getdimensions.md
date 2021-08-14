---
title: Funzione RWTexture1D::GetDimensions
description: Restituisce le dimensioni della risorsa. | Funzione RWTexture1D::GetDimensions
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
ms.openlocfilehash: eb779d071f471abe92b18ef456a2a016536a5231ccf327f8ebd175be8e5ff224
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509293"
---
# <a name="rwtexture1dgetdimensions-function"></a>Funzione RWTexture1D::GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Larghezza della risorsa, in texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nothing

## <a name="remarks"></a>Commenti

Questo è un elenco delle versioni di overload di questo metodo.


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
