---
title: errorf (funzione)
description: Invia un messaggio di errore alla coda delle informazioni.
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
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045602"
---
# <a name="errorf-function"></a>errorf (funzione)

Invia un messaggio di errore alla coda delle informazioni.

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

 

 




