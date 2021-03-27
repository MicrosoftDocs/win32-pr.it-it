---
title: 'Funzione RWStructuredBuffer:: Load (int, uint)'
description: "Legge i dati del buffer e restituisce lo stato dell'operazione. | Funzione RWStructuredBuffer:: Load (int, uint)"
ms.assetid: 19FAA031-F31E-4B73-BC69-489CDF0CF184
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74a153d4b56ec16b80dec180287005666747d259
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981250"
---
# <a name="rwstructuredbufferloadintuint-function"></a>Funzione RWStructuredBuffer:: Load (int, uint)

Legge i dati del buffer e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **int**

Posizione del buffer.

</dd> <dt>

*Stato* \[ di out\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features). Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Digitare:

Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load](rwstructuredbuffer-load.md)
</dt> </dl>

 

 
