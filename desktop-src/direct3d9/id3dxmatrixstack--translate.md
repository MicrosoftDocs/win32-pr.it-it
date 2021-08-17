---
description: 'Metodo ID3DXMATRIXStack::Translate (D3dx9math.h): determina il prodotto della matrice corrente e della matrice di traslazione calcolata determinata dai fattori specifici (x, y e z).'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: Metodo ID3DXMATRIXStack::Translate (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f51ed86569d29488f93a661999821c3f27bd5f17ed9ba2e552a2604f804c305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987221"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::Translate (D3dx9math.h)

Determina il prodotto della matrice corrente e la matrice di traslazione calcolata determinata dai fattori (x, y e z) specifici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Translate(
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

Questo metodo moltiplica a destra la matrice corrente con la matrice di traslazione calcolata (la trasformazione riguarda l'origine globale corrente).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
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

[**ID3DXMATRIXStack::TranslateLocal**](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
