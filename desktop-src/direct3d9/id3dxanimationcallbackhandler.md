---
description: "Un'applicazione implementa questa interfaccia per gestire i callback nei set di animazioni generati dalle chiamate a ID3DXAnimationController:: AdvanceTime."
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: Interfaccia ID3DXAnimationCallbackHandler (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3b58c58c6a0bd71924fb207170a177797b9f84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323509"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>Interfaccia ID3DXAnimationCallbackHandler

Un'applicazione implementa questa interfaccia per gestire i callback nei set di animazioni generati dalle chiamate a [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="members"></a>Membri

L'interfaccia **ID3DXAnimationCallbackHandler** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationCallbackHandler** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXAnimationCallbackHandler** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandleCallback**](id3dxanimationcallbackhandler--handlecallback.md) | L'applicazione implementa questo metodo. Questo metodo viene chiamato quando si verifica un callback per un set di animazioni in una delle tracce durante una chiamata a [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).<br/> |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXANIMATIONCALLBACKHANDLER è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
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

 

 
