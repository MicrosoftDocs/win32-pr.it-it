---
description: Questa interfaccia viene implementata dall'applicazione per allocare o liberare oggetti contenitore di frame e mesh. I metodi di questo metodo vengono chiamati durante il caricamento e l'eliminazione delle gerarchie dei frame.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interfaccia ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058678"
---
# <a name="id3dxallocatehierarchy-interface"></a>Interfaccia ID3DXAllocateHierarchy

Questa interfaccia viene implementata dall'applicazione per allocare o liberare oggetti contenitore di frame e mesh. I metodi di questo metodo vengono chiamati durante il caricamento e l'eliminazione delle gerarchie dei frame.

## <a name="members"></a>Membri

L'interfaccia **ID3DXAllocateHierarchy** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAllocateHierarchy** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXAllocateHierarchy** dispone di questi metodi.



| Metodo                                                                       | Descrizione                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | Richiede l'allocazione di un oggetto frame.<br/>            |
| [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md)   | Richiede l'allocazione di un oggetto contenitore mesh.<br/>   |
| [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)                 | Richiede la deallocazione di un oggetto frame.<br/>          |
| [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | Richiede la deallocazione di un oggetto contenitore mesh.<br/> |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXALLOCATEHIERARCHY è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
