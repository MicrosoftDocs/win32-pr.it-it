---
title: Funzione RWByteAddressBuffer::Load4(uint,uint)
description: Ottiene quattro valori e restituisce lo stato dell'operazione.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
keywords:
- Funzione Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f64fe84f17ee4cc1fed25b870b2142b474e753fa41e82cd0d385c9ef185ee9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672111"
---
# <a name="load4uintuint-function"></a>Funzione Load4(uint,uint)

Ottiene quattro valori e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ Pollici\]
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

Tipo: **uint4**

Quattro valori.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi Load4](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 