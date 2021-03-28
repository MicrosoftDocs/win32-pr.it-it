---
title: QuadReadAcrossY (funzione)
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
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976879"
---
# <a name="quadreadacrossy-function"></a>QuadReadAcrossY (funzione)

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

Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




