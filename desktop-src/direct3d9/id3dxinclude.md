---
description: ID3DXInclude è un'interfaccia implementata dall'utente per fornire callback per \# le direttive include durante la compilazione dello shader.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interfaccia ID3DXInclude (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e48ab32894ad1bf4c2f992ab4fff5953b3d98de4afd5e044de0119e056ee8133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295181"
---
# <a name="id3dxinclude-interface"></a>Interfaccia ID3DXInclude

ID3DXInclude è un'interfaccia implementata dall'utente per fornire callback per \# le direttive include durante la compilazione dello shader. Ognuno dei metodi in questa interfaccia deve essere implementato dall'utente che verrà quindi usato come callback per l'applicazione quando si verifica una delle condizioni seguenti:

-   Uno shader HLSL che contiene \# un'inclusione viene compilato chiamando una delle funzioni D3DXCompileShader. \* \* \*
-   Un assembly shader \# include viene assemblato chiamando una delle funzioni D3DXAssembleShader. \* \* \*
-   Un effetto che contiene un'inclusione viene compilato chiamando una delle funzioni \# D3DXCreateEffect o \* \* \* D3DXCreateEffectCompiler. \* \* \*

## <a name="members"></a>Membri

**L'interfaccia ID3DXInclude** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXInclude** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXInclude** include questi metodi.



| Metodo                               | Descrizione                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Chiudi**](id3dxinclude--close.md) | Metodo implementato dall'utente per la chiusura di un file di \# inclusione shader.<br/>                             |
| [**Aperto**](id3dxinclude--open.md)   | Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un file di inclusione \# shader.<br/> |



 

## <a name="remarks"></a>Commenti

Un utente crea un'interfaccia ID3DXInclude implementando una classe che deriva da questa interfaccia e implementando tutti i metodi di interfaccia.

Il tipo LPD3DXINCLUDE è definito come un puntatore a questa interfaccia.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
