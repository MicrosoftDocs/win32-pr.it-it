---
description: Ottiene il valore di scala dello schema stipple.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: Metodo ID3DXLine::GetPatternScale (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3799901d071da08ee1bb0de4994ed330fabe2d8fedf3b59ce556105f0a280e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675143"
---
# <a name="id3dxlinegetpatternscale-method"></a>Metodo ID3DXLine::GetPatternScale

Ottiene il valore di scala dello schema stipple.

## <a name="syntax"></a>Sintassi


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Restituisce il valore utilizzato per ridimensionare lo schema stipple. 1,0f è il valore predefinito e non rappresenta alcun ridimensionamento. Un valore minore di 1,0f riduce il modello e un valore maggiore di 1,0 estende il modello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
