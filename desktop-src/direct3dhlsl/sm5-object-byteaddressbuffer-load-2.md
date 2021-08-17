---
title: Funzione ByteAddressBuffer::Load(int, uint)
description: Ottiene un valore e lo stato dell'operazione.
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 09376ad3ed2af10d6f1a6d62c16a2b66afe47e845b544e33fef5dba8cf208fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725375"
---
# <a name="byteaddressbufferloadint-uint-function"></a>Funzione ByteAddressBuffer::Load(int, uint)

Ottiene un valore e lo stato dell'operazione.

## <a name="syntax"></a>Sintassi

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Indirizzo di input in byte, che deve essere un multiplo di 4.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint**

Un valore.

## <a name="remarks"></a>Commenti

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di caricamento](byteaddressbuffer-load.md)
</dt> <dt>

[**ByteAddressBuffer**](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
