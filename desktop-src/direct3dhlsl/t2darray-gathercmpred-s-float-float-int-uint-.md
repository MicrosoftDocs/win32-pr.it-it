---
title: 'Funzione Texture2DArray:: GatherCmpRed (S, float, float, int, uint)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto insieme allo stato del mapping dei riquadri. | Funzione Texture2DArray:: GatherCmpRed (S, float, float, int, uint)"
ms.assetid: 83974A85-26CB-4724-A60F-64F214800723
keywords:
- Funzione GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79743d4d2b30049a580309aa79bf6b3d79c73d3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981954"
---
# <a name="texture2darraygathercmpredsfloatfloatintuint-function"></a>Funzione Texture2DArray:: GatherCmpRed (S, float, float, int, uint)

Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto insieme allo stato del mapping dei riquadri.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

Indice del campionatore in base zero.

</dd> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **float**

Coordinate di esempio (u, v).

</dd> <dt>

*CompareValue* \[ in\]
</dt> <dd>

Tipo: **float**

Valore da confrontare con ogni valore campionato.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Tipo: **int**

Offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Stato* \[ di out\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features). Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo corrisponde al tipo di modello.

## <a name="remarks"></a>Commenti

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherCmpRed](texture2darray-gathercmpred.md)
</dt> </dl>

 

 
