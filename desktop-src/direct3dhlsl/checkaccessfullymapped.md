---
title: Funzione CheckAccessFullyMapped
description: Determina se a tutti i valori di un'operazione Sample, Gather o Load è stato eseguito l'accesso ai riquadri mappati in una risorsa affiancata.
ms.assetid: 2CAB7770-143E-4E29-A57F-96C27021AC5F
keywords:
- Funzione CheckAccessFullyMapped HLSL
topic_type:
- apiref
api_name:
- CheckAccessFullyMapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e7241fa5546edffb2b7c5ff36d2e43919e6d0b6fef9ff617c0fb63a674ffee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516674"
---
# <a name="checkaccessfullymapped-function"></a>Funzione CheckAccessFullyMapped

Determina se tutti i valori di **un'operazione Sample,** **Gather** o **Load** hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features)

## <a name="syntax"></a>Sintassi

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*stato* \[ Pollici\]
</dt> <dd>

Tipo: **solo \_ uint**

Valore di stato restituito da **un'operazione Sample,** **Gather** **o Load.** Poiché non è possibile accedere direttamente a questo valore di stato, è necessario passarlo a **CheckAccessFullyMapped**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce un **valore booleano** che indica se tutti i valori di un'operazione **Sample,** **Gather** o **Load** hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Restituisce **TRUE se** tutti i valori dell'operazione hanno eseguito l'accesso ai riquadri mappati; In caso contrario, restituisce **FALSE** se sono stati presi valori da un riquadro non mappato.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Modello shader 5 e](d3d11-graphics-reference-sm5.md) modelli shader superiori | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 