---
description: "Interfaccia ID3DXMATRIXStack: le applicazioni usano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici."
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interfaccia ID3DXMATRIXStack (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8fa483be72d29cc869b2bd468cff25033a80187bef69317af4894fc05b096dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856451"
---
# <a name="id3dxmatrixstack-interface"></a>Interfaccia ID3DXMATRIXStack

Le applicazioni usano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici.

## <a name="members"></a>Membri

**L'interfaccia ID3DXMATRIXStack** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXMATRIXStack** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXMATRIXStack** include questi metodi.



| Metodo                                                                       | Descrizione                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack--gettop.md)                                   | Recupera la matrice corrente all'inizio dello stack.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack--loadidentity.md)                       | Carica l'identità nella matrice corrente.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack--loadmatrix.md)                           | Carica la matrice specificata nella matrice corrente.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack--multmatrix.md)                           | Determina il prodotto della matrice corrente e della matrice specificata.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)                 | Determina il prodotto della matrice specificata e della matrice corrente.<br/>                                                              |
| [**Pop**](id3dxmatrixstack--pop.md)                                         | Rimuove la matrice corrente dall'inizio dello stack.<br/>                                                                           |
| [**Spingere**](id3dxmatrixstack--push.md)                                       | Aggiunge una matrice nello stack.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack--rotateaxis.md)                           | Ruota (rispetto allo spazio delle coordinate del mondo) intorno a un asse arbitrario.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)                 | Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)           | Ruota (rispetto allo spazio delle coordinate del mondo) intorno a un asse arbitrario.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.<br/>                                             |
| [**Scalabilità**](id3dxmatrixstack--scale.md)                                     | Ridimensionare la matrice corrente sull'origine delle coordinate del mondo.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack--scalelocal.md)                           | Ridimensionare la matrice corrente sull'origine dell'oggetto.<br/>                                                                               |
| [**Traduci**](id3dxmatrixstack--translate.md)                             | Determina il prodotto della matrice corrente e la matrice di traslazione calcolata determinata dai fattori (x, y e z) specifici.<br/> |
| [**TranslateLocal**](id3dxmatrixstack--translatelocal.md)                   | Determina il prodotto della matrice di traslazione calcolata determinata dai fattori (x, y e z) e dalla matrice corrente.<br/> |



 

## <a name="remarks"></a>Commenti

**L'interfaccia ID3DXMATRIXStack** viene ottenuta chiamando la [**funzione D3DXCreateMatrixStack.**](d3dxcreatematrixstack.md)

Il tipo LPD3DXMATRIXSTACK è definito come puntatore **all'interfaccia ID3DXMATRIXStack.**


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
