---
description: ID3DXInclude è un'interfaccia implementata dall'utente per fornire callback per le \# direttive include durante la compilazione dello shader.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interfaccia ID3DXInclude (D3DX9Shader. h)
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
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323531"
---
# <a name="id3dxinclude-interface"></a>Interfaccia ID3DXInclude

ID3DXInclude è un'interfaccia implementata dall'utente per fornire callback per le \# direttive include durante la compilazione dello shader. Ognuno dei metodi in questa interfaccia deve essere implementato dall'utente che verrà quindi utilizzato come callback all'applicazione quando si verifica una delle condizioni seguenti:

-   Uno shader HLSL che contiene un' \# inclusione viene compilato chiamando una delle \* \* \* funzioni D3DXCompileShader.
-   Un assembly shader \# include viene assemblato chiamando qualsiasi \* \* \* funzione D3DXAssembleShader.
-   Un effetto che contiene un' \# inclusione viene compilato da chiamando una delle funzioni D3DXCreateEffect \* \* \* o D3DXCreateEffectCompiler \* \* \* .

## <a name="members"></a>Membri

L'interfaccia **ID3DXInclude** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXInclude** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXInclude** dispone di questi metodi.



| Metodo                               | Descrizione                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Chiudi**](id3dxinclude--close.md) | Metodo implementato dall'utente per la chiusura di un \# file di inclusione dello shader.<br/>                             |
| [**Aprire**](id3dxinclude--open.md)   | Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un \# file di inclusione dello shader.<br/> |



 

## <a name="remarks"></a>Commenti

Un utente crea un'interfaccia ID3DXInclude implementando una classe che deriva da questa interfaccia e implementando tutti i metodi di interfaccia.

Il tipo LPD3DXINCLUDE è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
