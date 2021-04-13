---
description: L'interfaccia ID3DXEffectCompiler compila un effetto da una funzione o da un vertex shader.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interfaccia ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354344"
---
# <a name="id3dxeffectcompiler-interface"></a>Interfaccia ID3DXEffectCompiler

L'interfaccia **ID3DXEffectCompiler** compila un effetto da una funzione o da un vertex shader.

## <a name="members"></a>Membri

L'interfaccia **ID3DXEffectCompiler** eredita da [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffectCompiler** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXEffectCompiler** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | Compilare un effetto.<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | Compila uno shader da un effetto che contiene una o più funzioni.<br/>                                                            |
| [**GetLiteral**](id3dxeffectcompiler--getliteral.md)       | Ottiene uno stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.<br/>      |
| [**Valore letterale**](id3dxeffectcompiler--setliteral.md)       | Consente di abilitare o disabilitare lo stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia ID3DXEffectCompiler viene ottenuta chiamando [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)o [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).

Il tipo LPD3DXEFFECTCOMPILER è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




