---
description: 'Metodo ID3DXMATRIXStack::MultMatrix (D3dx9math.h): determina il prodotto della matrice corrente e della matrice specificata.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: Metodo ID3DXMATRIXStack::MultMatrix (D3dx9math.h)
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
ms.openlocfilehash: 7361223e8fbcbae0f81641718b216c5903ff6319
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093529"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::MultMatrix (D3dx9math.h)

Determina il prodotto della matrice corrente e della matrice specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMat* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) da moltiplicare con la matrice corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo moltiplica a destra la matrice specificata nella matrice corrente (la trasformazione riguarda l'origine globale corrente).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Questo metodo non aggiunge un elemento nello stack, ma sostituisce la matrice corrente con il prodotto della matrice corrente e la matrice specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




