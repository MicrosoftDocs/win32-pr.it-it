---
description: Le applicazioni utilizzano l'interfaccia ID3DXEffectPool per identificare i parametri che verranno condivisi tra gli effetti. Vedere condivisione di parametri in clonazione e condivisione (Direct3D 9). Questa interfaccia non dispone di metodi.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interfaccia ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401934"
---
# <a name="id3dxeffectpool-interface"></a>Interfaccia ID3DXEffectPool

Le applicazioni utilizzano l'interfaccia **ID3DXEffectPool** per identificare i parametri che verranno condivisi tra gli effetti. Vedere condivisione di parametri in [clonazione e condivisione (Direct3D 9)](cloning-and-sharing.md). Questa interfaccia non dispone di metodi.

## <a name="members"></a>Membri

L'interfaccia **ID3DXEffectPool** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="remarks"></a>Commenti

L'interfaccia ID3DXEffectPool viene ottenuta chiamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

Il tipo LPD3DXEFFECTPOOL è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
