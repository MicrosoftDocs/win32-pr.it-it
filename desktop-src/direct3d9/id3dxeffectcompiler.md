---
description: L'interfaccia ID3DXEffectCompiler compila un effetto da una funzione o da un vertex shader.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interfaccia ID3DXEffectCompiler (D3DX9Effect.h)
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
ms.openlocfilehash: c7a16417528d1adbd9ba54f9bd7120057654d14e0ef4bddad829e8f232445069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856741"
---
# <a name="id3dxeffectcompiler-interface"></a>Interfaccia ID3DXEffectCompiler

**L'interfaccia ID3DXEffectCompiler** compila un effetto da una funzione o da un vertex shader.

## <a name="members"></a>Membri

**L'interfaccia ID3DXEffectCompiler** eredita da [**ID3DXBaseEffect.**](id3dxbaseeffect.md) **ID3DXEffectCompiler** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXEffectCompiler** include questi metodi.



| Metodo                                                      | Descrizione                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | Compilare un effetto.<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | Compila uno shader da un effetto che contiene una o più funzioni.<br/>                                                            |
| [**GetLiteral**](id3dxeffectcompiler--getliteral.md)       | Ottiene lo stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.<br/>      |
| [**SetLiteral**](id3dxeffectcompiler--setliteral.md)       | Attiva o disattiva lo stato letterale di un parametro. Un parametro letterale ha un valore che non cambia durante la durata di un effetto.<br/> |



 

## <a name="remarks"></a>Commenti

L'interfaccia ID3DXEffectCompiler viene ottenuta chiamando [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)o [**D3DXCreateEffectCompilerFromResource.**](d3dxcreateeffectcompilerfromresource.md)

Il tipo LPD3DXEFFECTCOMPILER è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



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

 

 




