---
title: printf (funzione)
description: Invia un messaggio shader personalizzato alla coda di informazioni.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- funzione printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103956008"
---
# <a name="printf-function"></a>printf (funzione)

Invia un messaggio shader personalizzato alla coda di informazioni.

## <a name="syntax"></a>Sintassi

``` syntax
void printf(
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

*argomento...* 
</dt> <dd>

Argomenti facoltativi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione non esegue alcuna operazione nei dispositivi che non lo supportano.

### <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o versione successiva.](dx-graphics-hlsl-sm3.md) | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




