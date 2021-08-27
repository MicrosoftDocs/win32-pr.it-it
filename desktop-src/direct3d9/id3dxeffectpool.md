---
description: Le applicazioni usano l'interfaccia ID3DXEffectPool per identificare i parametri che verranno condivisi tra gli effetti. Vedere condivisione dei parametri in Clonazione e condivisione (Direct3D 9). Questa interfaccia non ha metodi.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interfaccia ID3DXEffectPool (D3DX9Effect.h)
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
ms.openlocfilehash: 42b7669d974fffde76c8c8f1e7beb4f8d78bf58fda3810130b255d4bc5a693df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118681"
---
# <a name="id3dxeffectpool-interface"></a>Interfaccia ID3DXEffectPool

Le applicazioni usano **l'interfaccia ID3DXEffectPool** per identificare i parametri che verranno condivisi tra gli effetti. Vedere la condivisione dei parametri in [Clonazione e condivisione (Direct3D 9).](cloning-and-sharing.md) Questa interfaccia non ha metodi.

## <a name="members"></a>Membri

**L'interfaccia ID3DXEffectPool** eredita dall'interfaccia [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

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
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
