---
title: Funzione RWByteAddressBuffer::Load3(uint,uint)
description: Ottiene tre valori e restituisce lo stato dell'operazione.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
keywords:
- Funzione Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91d4a90094d93705e17c9087583974ef8f9d76e1878cb0c5aa8dab21dc82e073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791223"
---
# <a name="load3uintuint-function"></a>Funzione Load3(uint,uint)

Ottiene tre valori e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Località* \[ Pollici\]
</dt> <dd>

Tipo: **uint**

Posizione del buffer.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint3**

Tre valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load3](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 