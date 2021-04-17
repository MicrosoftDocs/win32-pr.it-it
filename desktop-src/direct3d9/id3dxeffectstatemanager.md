---
description: Si tratta di un'interfaccia implementata dall'utente che consente a un utente di impostare lo stato del dispositivo da un effetto.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interfaccia ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355229"
---
# <a name="id3dxeffectstatemanager-interface"></a>Interfaccia ID3DXEffectStateManager

Si tratta di un'interfaccia implementata dall'utente che consente a un utente di impostare lo stato del dispositivo da un effetto. Ognuno dei metodi in questa interfaccia deve essere implementato dall'utente e sarà quindi utilizzato come callback all'applicazione quando si verifica una delle condizioni seguenti:

-   Un effetto chiama [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   Lo stato dell'effetto viene aggiornato dinamicamente chiamando l'API di modifica dello stato appropriato. Per informazioni dettagliate, vedere singole pagine dei metodi.

Quando un'applicazione usa il gestore degli Stati per implementare callback personalizzati, un effetto non salva più automaticamente e ripristina lo stato quando si chiamano [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md). Poiché l'applicazione ha implementato un comportamento di salvataggio e ripristino personalizzato nei callback, questo comportamento automatico viene ignorato.

## <a name="members"></a>Membri

L'interfaccia **ID3DXEffectStateManager** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXEffectStateManager** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXEffectStateManager** dispone di questi metodi.



| Metodo                                                                                | Descrizione                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Alleggeribile**](id3dxeffectstatemanager--lightenable.md)                           | Funzione di callback che deve essere implementata da un utente per abilitare o disabilitare una luce.<br/>                                 |
| [**SetFVF**](id3dxeffectstatemanager--setfvf.md)                                     | Funzione di callback che deve essere implementata da un utente per impostare un codice FVF.<br/>                                         |
| [**Chiaro**](id3dxeffectstatemanager--setlight.md)                                 | Funzione di callback che deve essere implementata da un utente per impostare una luce.<br/>                                            |
| [**Materiali**](id3dxeffectstatemanager--setmaterial.md)                           | Funzione di callback che deve essere implementata da un utente per impostare lo stato del materiale.<br/>                                     |
| [**SetNPatchMode**](id3dxeffectstatemanager--setnpatchmode.md)                       | Funzione di callback che deve essere implementata da un utente per impostare il numero di segmenti di suddivisione per N-patch.<br/>   |
| [**SetPixelShader**](id3dxeffectstatemanager--setpixelshader.md)                     | Funzione di callback che deve essere implementata da un utente per impostare un pixel shader.<br/>                                     |
| [**SetPixelShaderConstantB**](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane del vertex shader.<br/>        |
| [**SetPixelShaderConstantF**](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.<br/> |
| [**SetPixelShaderConstantI**](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.<br/>        |
| [**SetRenderState**](id3dxeffectstatemanager--setrenderstate.md)                     | Funzione di callback che deve essere implementata da un utente per impostare lo stato di rendering.<br/>                                       |
| [**SetSamplerState**](id3dxeffectstatemanager--setsamplerstate.md)                   | Funzione di callback che deve essere implementata da un utente per impostare un campionatore.<br/>                                          |
| [**SetTexture**](id3dxeffectstatemanager--settexture.md)                             | Funzione di callback che deve essere implementata da un utente per impostare una trama.<br/>                                          |
| [**SetTextureStageState**](id3dxeffectstatemanager--settexturestagestate.md)         | Funzione di callback che deve essere implementata da un utente per impostare lo stato della fase della trama.<br/>                            |
| [**SetTransform**](id3dxeffectstatemanager--settransform.md)                         | Funzione di callback che deve essere implementata da un utente per impostare una trasformazione.<br/>                                        |
| [**SetVertexShader**](id3dxeffectstatemanager--setvertexshader.md)                   | Funzione di callback che deve essere implementata da un utente per impostare un vertex shader.<br/>                                    |
| [**SetVertexShaderConstantB**](id3dxeffectstatemanager--setvertexshaderconstantb.md) | Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane del vertex shader.<br/>        |
| [**SetVertexShaderConstantF**](id3dxeffectstatemanager--setvertexshaderconstantf.md) | Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.<br/> |
| [**SetVertexShaderConstantI**](id3dxeffectstatemanager--setvertexshaderconstanti.md) | Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.<br/>        |



 

## <a name="remarks"></a>Commenti

Un utente crea un'interfaccia ID3DXEffectStateManager implementando una classe che deriva da questa interfaccia e implementando tutti i metodi di interfaccia. Una volta creata l'interfaccia, è possibile ottenere o impostare il gestore di stato all'interno di un effetto usando [**ID3DXEffect:: GetStateManager**](id3dxeffect--getstatemanager.md) e [**ID3DXEffect:: SetStateManager**](id3dxeffect--setstatemanager.md).

Il tipo LPD3DXEFFECTSTATEMANAGER è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
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

 

 
