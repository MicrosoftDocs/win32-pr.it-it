---
description: Determina il prodotto della matrice specificata e della matrice corrente.
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235209"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a>Metodo ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)

Determina il prodotto della matrice specificata e della matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PM* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura D3DXMATRIX da moltiplicare con la matrice corrente.

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
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
