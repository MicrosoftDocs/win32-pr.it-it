---
title: Funzione QuadReadAcrossY
description: Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Funzione QuadReadAcrossY HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f761a3588759e0c27143d16bd8fac5f674f05ae1819a0cdcebc55d6b4bdc6e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672401"
---
# <a name="quadreadacrossy-function"></a>Funzione QuadReadAcrossY

Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y.

## <a name="syntax"></a>Sintassi

``` syntax
<type> QuadReadAcrossY(
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

Valore di origine specificato. Se la corsia di origine è inattiva, i risultati non sono definiti.

## <a name="remarks"></a>Commenti

Per altre informazioni sui quad, vedere [Panoramica del modello shader 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Questa funzione è supportata dal modello shader 6.0 solo in pixel e compute shader.



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




