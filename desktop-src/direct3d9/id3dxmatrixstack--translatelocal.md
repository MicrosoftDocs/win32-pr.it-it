---
description: 'Metodo ID3DXMATRIXStack::TranslateLocal (D3dx9math.h): determina il prodotto della matrice di traslazione calcolata determinata dai fattori (x, y e z) e dalla matrice corrente.'
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: Metodo ID3DXMATRIXStack::TranslateLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39984fa20ab0fa84d9b22b86fade2eb59277dd6a919c5bfa8d8a52efd33b1cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493121"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::TranslateLocal (D3dx9math.h)

Determina il prodotto della matrice di traslazione calcolata determinata dai fattori (x, y e z) e dalla matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di traslazione nella direzione x.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di traslazione nella direzione y.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di traslazione nella direzione z.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo moltiplica a sinistra la matrice corrente con la matrice di traslazione calcolata (la trasformazione riguarda l'origine locale dell'oggetto).


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::Translate**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
