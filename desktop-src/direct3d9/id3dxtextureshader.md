---
description: Interfaccia ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interfaccia ID3DXTextureShader (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95e6a8feb35ea5d1e38a5cb63bb1379e4995e7562839cc1b582ee8efd8550212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846981"
---
# <a name="id3dxtextureshader-interface"></a>Interfaccia ID3DXTextureShader

Interfaccia ID3DXTextureShader.

## <a name="members"></a>Membri

**L'interfaccia ID3DXTextureShader** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXTextureShader** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXTextureShader** include questi metodi.



| Metodo                                                                                       | Descrizione                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**GetConstant**](id3dxtextureshader--getconstant.md)                                       | Ottiene una costante cercandone l'indice.<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Ottenere un puntatore alla tabella delle costanti.<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | Ottiene una costante cercandone il nome.<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.<br/>  |
| [**GetConstantElement**](id3dxtextureshader--getconstantelement.md)                         | Ottenere una costante dalla tabella delle costanti.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Ottiene una descrizione della tabella delle costanti.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Ottiene un puntatore al flusso DWORD della funzione.<br/>                     |
| [**SetBool**](id3dxtextureshader--setbool.md)                                               | Imposta un valore BOOL.<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | Imposta una matrice di valori BOOL.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Imposta le costanti ai valori predefiniti dichiarati nello shader.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Imposta un numero a virgola mobile.<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | Imposta una matrice di numeri a virgola mobile.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Imposta un valore intero.<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | Imposta una matrice di numeri interi.<br/>                                       |
| [**SetMatrix**](id3dxtextureshader--setmatrix.md)                                           | Imposta una matrice non trasposta.<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | Imposta una matrice di matrici non trasposte.<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Imposta una matrice di puntatori a matrici non trasposte.<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | Imposta una matrice trasposta.<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | Imposta una matrice di matrici trasposte.<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Imposta una matrice di puntatori alle matrici trasposte.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Imposta la tabella costante con i dati nel buffer.<br/>             |
| [**SetVector**](id3dxtextureshader--setvector.md)                                           | Imposta un vettore 4D.<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | Imposta una matrice di vettori 4D.<br/>                                     |



 

## <a name="remarks"></a>Commenti

**L'interfaccia ID3DXTextureShader** viene ottenuta chiamando la [**funzione D3DXCreateTextureShader.**](d3dxcreatetextureshader.md)

**L'interfaccia ID3DXTextureShader,** come tutte le interfacce COM, eredita l'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Il tipo LPD3DXTEXTURESHADER è definito come puntatore **all'interfaccia ID3DXTextureShader.**


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
