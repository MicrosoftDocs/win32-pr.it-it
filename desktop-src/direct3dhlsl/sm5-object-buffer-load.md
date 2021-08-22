---
title: Funzione Buffer::Load(int, uint)
description: Legge i dati del buffer e restituisce lo stato dell'operazione. | Funzione Buffer::Load(int, uint)
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
keywords:
- Caricare la funzione HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 091cda0570f288139a1aa57eb53755897ed9089d17a598da7b13d2873c5bd70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845761"
---
# <a name="bufferloadint-uint-function"></a>Funzione Buffer::Load(int, uint)

Legge i dati del buffer e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Posizione del buffer.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per [**l'oggetto Buffer.**](sm5-object-buffer.md)

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="examples"></a>Esempio

In questo esempio viene illustrato come usare **Load**:

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](buffer-load.md)
</dt> </dl>

 

 
