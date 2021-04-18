---
description: Interfaccia ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interfaccia ID3DXTextureShader (D3DX9Shader. h)
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
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322544"
---
# <a name="id3dxtextureshader-interface"></a>Interfaccia ID3DXTextureShader

Interfaccia ID3DXTextureShader.

## <a name="members"></a>Membri

L'interfaccia **ID3DXTextureShader** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureShader** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXTextureShader** dispone di questi metodi.



| Metodo                                                                                       | Descrizione                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**Getcostante**](id3dxtextureshader--getconstant.md)                                       | Ottiene una costante cercando il relativo indice.<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Ottenere un puntatore alla tabella delle costanti.<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | Ottiene una costante cercandone il nome.<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.<br/>  |
| [**Getconstantelement**](id3dxtextureshader--getconstantelement.md)                         | Ottenere una costante dalla tabella delle costanti.<br/>                          |
| [**Getdesc**](id3dxtextureshader--getdesc.md)                                               | Ottiene una descrizione della tabella delle costanti.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Ottiene un puntatore al flusso DWORD della funzione.<br/>                     |
| [**DiBOOL**](id3dxtextureshader--setbool.md)                                               | Imposta un valore BOOL.<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | Imposta una matrice di valori BOOL.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Imposta le costanti sui valori predefiniti dichiarati nello shader.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Imposta un numero a virgola mobile.<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | Imposta una matrice di numeri a virgola mobile.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Imposta un valore integer.<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | Imposta una matrice di numeri interi.<br/>                                       |
| [**Sematrix**](id3dxtextureshader--setmatrix.md)                                           | Imposta una matrice non trasposta.<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | Imposta una matrice di matrici non transposte.<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Imposta una matrice di puntatori a matrici non trasposte.<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | Imposta una matrice trasposta.<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | Imposta una matrice di matrici trasposte.<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Imposta una matrice di puntatori a matrici trasposte.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Imposta la tabella delle costanti con i dati nel buffer.<br/>             |
| [**Sevector**](id3dxtextureshader--setvector.md)                                           | Imposta un vettore 4D.<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | Imposta una matrice di vettori 4D.<br/>                                     |



 

## <a name="remarks"></a>Commenti

L'interfaccia **ID3DXTextureShader** viene ottenuta chiamando la funzione [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .

L'interfaccia **ID3DXTextureShader** , come tutte le interfacce com, eredita l'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Il tipo LPD3DXTEXTURESHADER è definito come puntatore all'interfaccia **ID3DXTextureShader** .


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
