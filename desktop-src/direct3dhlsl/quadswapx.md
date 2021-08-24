---
title: Funzione QuadReadAcrossX
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
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672441"
---
# <a name="quadreadacrossx-function"></a>Funzione QuadReadAcrossX

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

Per altre informazioni sui quad, vedere [Panoramica del modello shader 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Questa funzione è supportata dal modello di shader 6.0 solo in pixel e compute shader.



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




