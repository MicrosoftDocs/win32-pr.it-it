---
title: QuadReadLaneAt (funzione)
description: Restituisce il valore di origine specificato dalla corsia identificata dall'ID della corsia all'interno del Quad corrente.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Funzione QuadReadLaneAt HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474645"
---
# <a name="quadreadlaneat-function"></a>QuadReadLaneAt (funzione)

Restituisce il valore di origine specificato dalla corsia identificata dall'ID della corsia all'interno del Quad corrente.

## <a name="syntax"></a>Sintassi


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Valore* 
</dt> <dd>

Tipo richiesto.

</dd> <dt>

*quadLaneID* 
</dt> <dd>

ID corsia; si tratta di un valore compreso tra 0 e 3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore di origine specificato. Il risultato di questa funzione è uniforme nel quad. Se la corsia di origine è inattiva, i risultati non sono definiti.

## <a name="remarks"></a>Commenti

Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




