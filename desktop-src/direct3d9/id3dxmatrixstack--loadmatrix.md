---
description: 'Metodo ID3DXMATRIXStack::LoadMatrix (D3dx9math.h): carica la matrice specificata nella matrice corrente.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: Metodo ID3DXMATRIXStack::LoadMatrix (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093539"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::LoadMatrix (D3dx9math.h)

Carica la matrice specificata nella matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMat* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) caricata nella matrice corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Si noti che questo metodo non aggiunge un elemento nello stack. sostituisce invece la matrice corrente con la matrice fornita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




