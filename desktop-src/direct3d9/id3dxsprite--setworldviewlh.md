---
description: Imposta la trasformazione di visualizzazione del mondo mancino per uno sprite. Una chiamata a questo metodo è necessaria prima dell'ordinamento o dell'ordinamento degli sprite.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: Metodo ID3DXSprite::SetWorldViewLH (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67ee276b90629a18f93bd9a26879e8a7ad62d71ae46baf2d2c0a6bfba82a53a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292573"
---
# <a name="id3dxspritesetworldviewlh-method"></a>Metodo ID3DXSprite::SetWorldViewLH

Imposta la trasformazione di visualizzazione del mondo mancino per uno sprite. Una chiamata a questo metodo è necessaria prima dell'ordinamento o dell'ordinamento degli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWorld* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**un oggetto D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione del mondo. Se **NULL,** la matrice di identità viene usata per la trasformazione globale.

</dd> <dt>

*pView* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**un oggetto D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione di visualizzazione. Se **NULL,** la matrice di identità viene usata per la trasformazione della visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

È necessaria una chiamata a questo metodo (o a [**ID3DXSprite::SetWorldViewRH)**](id3dxsprite--setworldviewrh.md)se il rendering dello sprite verrà eseguito con il valore del flag [D3DXSprite \_ \_ ROLLBACK,](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH \_ FRONTTOBACK o \_ D3DXSprite \_ \_ SORT DEPTH \_ \_ BACKTOFRONT in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




