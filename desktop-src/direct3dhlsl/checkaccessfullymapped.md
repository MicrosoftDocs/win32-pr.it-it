---
title: CheckAccessFullyMapped (funzione)
description: Determina se tutti i valori di un'operazione di esempio, di raccolta o di caricamento hanno eseguito l'accesso ai riquadri mappati in una risorsa affiancata.
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
ms.openlocfilehash: c7310e0ebac496fc8f5a56ba3843b7496b8ce7c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729370"
---
# <a name="checkaccessfullymapped-function"></a>CheckAccessFullyMapped (funzione)

Determina se tutti i valori di un'operazione di **esempio**, di **raccolta** o di **caricamento** hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).

## <a name="syntax"></a>Sintassi

``` syntax
bool CheckAccessFullyMapped(
  in uint_only status
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*stato* \[ di in\]
</dt> <dd>

Tipo: **\_ solo uint**

Valore di stato restituito da un'operazione di **esempio**, **raccolta** o **caricamento** . Poiché non è possibile accedere direttamente a questo valore di stato, è necessario passarlo a **CheckAccessFullyMapped**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce un valore **booleano** che indica se tutti i valori di un'operazione di **esempio**, di **raccolta** o di **caricamento** hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features). Restituisce **true** se tutti i valori dell'operazione hanno eseguito l'accesso ai riquadri mappati; in caso contrario, restituisce **false** se sono stati rilevati valori da un riquadro non mappato.

## <a name="remarks"></a>Commenti

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì       |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 