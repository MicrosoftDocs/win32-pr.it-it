---
title: 'Funzione Texture2D:: GatherAlpha (S, float, int2, int2, int2, int2, uint)'
description: "Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri. | Funzione Texture2D:: GatherAlpha (S, float, int2, int2, int2, int2, uint)"
ms.assetid: C088BC6A-397C-4702-9BFA-0B2F10C833BD
keywords:
- Funzione GatherAlpha HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fddf9ebc8358bfc911f05d1f6e0cb34e8cfb5da
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353536"
---
# <a name="texture2dgatheralphasfloatint2int2int2int2uint-function"></a>Funzione Texture2D:: GatherAlpha (S, float, int2, int2, int2, int2, uint)

Restituisce i componenti alfa dei quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
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

*Offset1* \[ in\]
</dt> <dd>

Tipo: **int2**

Primo componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Offset2* \[ in\]
</dt> <dd>

Tipo: **int2**

Secondo componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Offset3* \[ in\]
</dt> <dd>

Tipo: **int2**

Terzo componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Offset4* \[ in\]
</dt> <dd>

Tipo: **int2**

Quarto componente di offset applicato alle coordinate di trama prima del campionamento.

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

[Metodi GatherAlpha](texture2d-gatheralpha.md)
</dt> </dl>

 

 
