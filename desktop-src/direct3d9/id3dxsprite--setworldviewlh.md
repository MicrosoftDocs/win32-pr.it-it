---
description: Imposta la trasformazione di visualizzazione globale a sinistra per uno sprite. È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'Metodo ID3DXSprite:: SetWorldViewLH (D3dx9core. h)'
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
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235080"
---
# <a name="id3dxspritesetworldviewlh-method"></a>Metodo ID3DXSprite:: SetWorldViewLH

Imposta la trasformazione di visualizzazione globale a sinistra per uno sprite. È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWorld* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a un [**D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione globale. Se è **null**, la matrice di identità viene utilizzata per la trasformazione globale.

</dd> <dt>

*pview* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a un [**D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione visualizzazione. Se è **null**, la matrice di identità viene utilizzata per la trasformazione della vista.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR

## <a name="remarks"></a>Commenti

Una chiamata a questo metodo (o a [**ID3DXSprite:: SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) è obbligatoria se verrà eseguito il rendering dello sprite con [D3DXSprite \_ \_ Billboard](d3dxsprite.md), D3DXSprite \_ \_ Sort \_ Depth \_ FRONTTOBACK o D3DXSprite \_ \_ Sort \_ Depth \_ BACKTOFRONT flag value in [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




