---
title: Funzione Texture2DMS::GetDimensions
description: Restituisce le dimensioni della risorsa. | Funzione Texture2DMS::GetDimensions
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: dbe034b6484b80efb58712196c4bd4d0aa67800c51f659c97b0d400e934eeecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985831"
---
# <a name="texture2dmsgetdimensions-function"></a>Funzione Texture2DMS::GetDimensions

Restituisce le dimensioni della risorsa.

## <a name="syntax"></a>Sintassi

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

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

*NumberOfSamples* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di posizioni di esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo è un elenco delle versioni di overload di questo metodo.


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
