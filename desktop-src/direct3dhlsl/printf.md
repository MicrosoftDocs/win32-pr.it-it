---
title: printf (funzione)
description: Invia un messaggio shader personalizzato alla coda di informazioni.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- Funzione printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47131cacef436572f519b394a02b4aaa357a426dd80a192868712cb3d7779e24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672521"
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

*discussione...* 
</dt> <dd>

Argomenti facoltativi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa operazione non esegue alcuna operazione nei dispositivi che non la supportano.

### <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) o versione successiva.](dx-graphics-hlsl-sm3.md) | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni intrinseche](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




