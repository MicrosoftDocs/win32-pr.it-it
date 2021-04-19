---
description: Determina il prodotto della matrice corrente e della matrice specificata.
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'Metodo ID3DXMATRIXStack:: MultMatrix (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322335"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack:: MultMatrix (D3dx9math. h)

Determina il prodotto della matrice corrente e della matrice specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMat* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) da moltiplicare con la matrice corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo moltiplica la matrice specificata con la matrice corrente (la trasformazione è relativa all'origine mondiale corrente).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Questo metodo non aggiunge un elemento allo stack, ma sostituisce la matrice corrente con il prodotto della matrice corrente e della matrice specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




