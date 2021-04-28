---
description: "Metodo ID3DXMATRIXStack::P op (D3dx9math.h): rimuove la matrice corrente dall'inizio dello stack."
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: Metodo ID3DXMATRIXStack::P op (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093504"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::P op (D3dx9math.h)

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
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::GetTop**](id3dxmatrixstack--gettop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P ush**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




