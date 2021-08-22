---
title: Funzione errorf
description: Invia un messaggio di errore alla coda di informazioni.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- funzione errorf HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0651a27419a369721806e9aa4717a20088f8f5fbbaa0063628d2feb69648c7cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562681"
---
# <a name="errorf-function"></a>Funzione errorf

Invia un messaggio di errore alla coda di informazioni.

## <a name="syntax"></a>Sintassi

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*format* 
</dt> <dd>

Stringa di formato.

</dd> <dt>

*discussione...* 
</dt> <dd>

Argomenti facoltativi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione non esegue alcuna operazione nei dispositivi che non la supportano.

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o versione successiva.](dx-graphics-hlsl-sm3.md) | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




