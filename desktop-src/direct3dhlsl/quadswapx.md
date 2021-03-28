---
title: QuadReadAcrossX (funzione)
description: Restituisce il valore locale specificato letto dall'altra corsia in questo quad nella direzione X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Funzione QuadReadAcrossX HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118662"
---
# <a name="quadreadacrossx-function"></a>QuadReadAcrossX (funzione)

Restituisce il valore locale specificato letto dall'altra corsia in questo quad nella direzione X.

## <a name="syntax"></a>Sintassi

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*localValue* 
</dt> <dd>

Tipo richiesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore locale specificato. Se la corsia di origine è inattiva, i risultati non sono definiti.

## <a name="remarks"></a>Commenti

Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




