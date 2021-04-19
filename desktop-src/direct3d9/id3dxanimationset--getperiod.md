---
description: Ottiene il periodo del set di animazioni.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'Metodo ID3DXAnimationSet:: GetPeriod (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323620"
---
# <a name="id3dxanimationsetgetperiod-method"></a>Metodo ID3DXAnimationSet:: GetPeriod

Ottiene il periodo del set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Periodo del set di animazioni.

## <a name="remarks"></a>Commenti

Il periodo è l'intervallo di tempo in cui i fotogrammi chiave dell'animazione sono validi. Per le animazioni di ciclo, questo è il periodo del ciclo. Le unità di tempo in cui sono specificati i fotogrammi chiave (ad esempio, secondi) sono determinate dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
