---
description: Imposta la trasformazione di visualizzazione a destra per uno sprite. Una chiamata a questo metodo è necessaria prima dell'ordinamento o dell'ordinamento degli sprite.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: Metodo ID3DXSprite::SetWorldViewRH (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 54da854fff0aeb2001e674218a7e7868971a6cf43af7bc00606b124c3f082b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800419"
---
# <a name="id3dxspritesetworldviewrh-method"></a>Metodo ID3DXSprite::SetWorldViewRH

Imposta la trasformazione di visualizzazione a destra per uno sprite. Una chiamata a questo metodo è necessaria prima dell'ordinamento o dell'ordinamento degli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWorldViewRH(
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

È necessaria una chiamata a questo metodo (o a [**ID3DXSprite::SetWorldViewLH)**](id3dxsprite--setworldviewlh.md)se il rendering dello sprite verrà eseguito con il valore del flag [D3DXSprite \_ \_ ROLLBACK,](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH \_ FRONTTOBACK o \_ D3DXSprite \_ \_ SORT DEPTH \_ \_ BACKTOFRONT in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




