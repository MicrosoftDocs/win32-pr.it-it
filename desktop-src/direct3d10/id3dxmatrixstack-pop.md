---
description: "Metodo ID3DXMATRIXStack::P op (D3DX10.h): rimuove la matrice corrente dall'inizio dello stack."
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: Metodo ID3DXMATRIXStack::P op (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6d559dc8a04500b4b208a87bcbda6841c21bf7c6e30f662a01cf943de286652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117735999"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a>Metodo ID3DXMATRIXStack::P op (D3DX10.h)

Rimuove la matrice corrente dall'inizio dello stack.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.

## <a name="remarks"></a>Commenti

Si noti che questo metodo decrementa il numero di elementi nello stack di 1, rimuovendo in modo efficace la matrice corrente dall'inizio dello stack e innalzando di livello una matrice all'inizio dello stack. Se il numero corrente di elementi nello stack è 0, questo metodo restituisce senza eseguire alcuna azione. Se il numero corrente di elementi nello stack è 1, questo metodo svuota lo stack.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




