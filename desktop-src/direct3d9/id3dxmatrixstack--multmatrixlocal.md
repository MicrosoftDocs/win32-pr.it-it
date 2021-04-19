---
description: Determina il prodotto della matrice specificata e della matrice corrente.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: 'Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 547856e01cfdcb79110780136c1bbab59c0d7073
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322334"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3dx9math. h)

Determina il prodotto della matrice specificata e della matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MultMatrixLocal(
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

Questo metodo consente di moltiplicare la matrice specificata con la matrice corrente (la trasformazione è relativa all'origine locale dell'oggetto).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Questo metodo non aggiunge un elemento allo stack, sostituisce la matrice corrente con il prodotto della matrice specificata e della matrice corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




