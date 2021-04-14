---
description: Ottiene il valore della scala del pattern stipple.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'Metodo ID3DXLine:: GetPatternScale (D3dx9core. h)'
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
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402030"
---
# <a name="id3dxlinegetpatternscale-method"></a>Metodo ID3DXLine:: GetPatternScale

Ottiene il valore della scala del pattern stipple.

## <a name="syntax"></a>Sintassi


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Restituisce il valore usato per ridimensionare il pattern stipple. 1,0 f è il valore predefinito e non rappresenta alcun ridimensionamento. Un valore inferiore a 1,0 f compatta il criterio e un valore maggiore di 1,0 estende il modello.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
