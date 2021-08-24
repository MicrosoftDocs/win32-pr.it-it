---
description: Fornisce metodi per ottenere e impostare i parametri degli effetti, ad esempio costanti, funzioni, shader e tecniche.
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: Interfaccia ID3DXBaseEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8525a8139cd769a59886576f8ec32c7dab333a2903ffdb0fba1abc8ffbe27d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848551"
---
# <a name="id3dxbaseeffect-interface"></a>Interfaccia ID3DXBaseEffect

Fornisce metodi per ottenere e impostare i parametri degli effetti, ad esempio costanti, funzioni, shader e tecniche.

## <a name="members"></a>Membri

**L'interfaccia ID3DXBaseEffect** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXBaseEffect** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXBaseEffect** include questi metodi.



| Metodo                                                                                    | Descrizione                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnnotation**](id3dxbaseeffect--getannotation.md)                                   | Ottiene l'handle di un'annotazione. <br/>                                                                                                                                                                                     |
| [**GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md)                       | Ottiene l'handle di un'annotazione cercandone il nome.<br/>                                                                                                                                                               |
| [**GetBool**](id3dxbaseeffect--getbool.md)                                               | Ottiene un valore BOOL.<br/>                                                                                                                                                                                                     |
| [**GetBoolArray**](id3dxbaseeffect--getboolarray.md)                                     | Ottiene una matrice di valori BOOL.<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | Ottiene la descrizione dell'effetto.<br/>                                                                                                                                                                                           |
| [**Getfloat**](id3dxbaseeffect--getfloat.md)                                             | Ottiene un valore a virgola mobile.<br/>                                                                                                                                                                                           |
| [**GetFloatArray**](id3dxbaseeffect--getfloatarray.md)                                   | Ottiene una matrice di valori a virgola mobile.<br/>                                                                                                                                                                                |
| [**GetFunction**](id3dxbaseeffect--getfunction.md)                                       | Ottiene l'handle di una funzione.<br/>                                                                                                                                                                                         |
| [**GetFunctionByName**](id3dxbaseeffect--getfunctionbyname.md)                           | Ottiene l'handle di una funzione cercandone il nome.<br/>                                                                                                                                                                  |
| [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)                               | Ottiene una descrizione della funzione.<br/>                                                                                                                                                                                           |
| [**Getint**](id3dxbaseeffect--getint.md)                                                 | Ottiene un numero intero.<br/>                                                                                                                                                                                                       |
| [**GetIntArray**](id3dxbaseeffect--getintarray.md)                                       | Ottiene una matrice di numeri interi.<br/>                                                                                                                                                                                             |
| [**GetMatrix**](id3dxbaseeffect--getmatrix.md)                                           | Ottiene una matrice non trasposta.<br/>                                                                                                                                                                                           |
| [**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)                                 | Ottiene una matrice di matrici non trasposte.<br/>                                                                                                                                                                               |
| [**GetMatrixPointerArray**](id3dxbaseeffect--getmatrixpointerarray.md)                   | Ottiene una matrice di puntatori a matrici non trasposte.<br/>                                                                                                                                                                   |
| [**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)                         | Ottiene una matrice trasposta.<br/>                                                                                                                                                                                              |
| [**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)               | Ottiene una matrice di matrici trasposte.<br/>                                                                                                                                                                                  |
| [**GetMatrixTransposePointerArray**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | Ottiene una matrice di puntatori alle matrici trasposte.<br/>                                                                                                                                                                      |
| [**GetParameter**](id3dxbaseeffect--getparameter.md)                                     | Ottiene l'handle di un parametro di primo livello o di un parametro membro della struttura.<br/>                                                                                                                                              |
| [**GetParameterByName**](id3dxbaseeffect--getparameterbyname.md)                         | Ottiene l'handle di un parametro di primo livello o di un parametro membro della struttura cercandone il nome.<br/>                                                                                                                       |
| [**GetParameterBySemantic**](id3dxbaseeffect--getparameterbysemantic.md)                 | Ottiene l'handle di un parametro di primo livello o di un parametro membro della struttura cercandone la semantica con una ricerca senza distinzione tra maiuscole e minuscole.<br/>                                                                                    |
| [**GetParameterDesc**](id3dxbaseeffect--getparameterdesc.md)                             | Ottiene una descrizione di parametro o annotazione.<br/>                                                                                                                                                                            |
| [**GetParameterElement**](id3dxbaseeffect--getparameterelement.md)                       | Ottiene l'handle di un parametro dell'elemento della matrice.<br/>                                                                                                                                                                          |
| [**GetPass**](id3dxbaseeffect--getpass.md)                                               | Ottiene l'handle di un passaggio.<br/>                                                                                                                                                                                             |
| [**GetPassByName**](id3dxbaseeffect--getpassbyname.md)                                   | Ottiene l'handle di un passaggio cercandone il nome.<br/>                                                                                                                                                                      |
| [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)                                       | Ottiene una descrizione del passaggio.<br/>                                                                                                                                                                                               |
| [**GetPixelShader**](id3dxbaseeffect--getpixelshader.md)                                 | Ottiene un pixel shader.<br/>                                                                                                                                                                                                   |
| [**Getstring**](id3dxbaseeffect--getstring.md)                                           | Ottiene una stringa.<br/>                                                                                                                                                                                                         |
| [**GetTechnique**](id3dxbaseeffect--gettechnique.md)                                     | Ottiene l'handle di una tecnica.<br/>                                                                                                                                                                                        |
| [**GetTechniqueByName**](id3dxbaseeffect--gettechniquebyname.md)                         | Ottiene l'handle di una tecnica cercandone il nome.<br/>                                                                                                                                                                 |
| [**GetTechniqueDesc**](id3dxbaseeffect--gettechniquedesc.md)                             | Ottiene una descrizione tecnica.<br/>                                                                                                                                                                                          |
| [**GetTexture**](id3dxbaseeffect--gettexture.md)                                         | Ottiene una trama.<br/>                                                                                                                                                                                                        |
| [**Getvalue**](id3dxbaseeffect--getvalue.md)                                             | Ottiene il valore di un parametro o un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. Questo metodo può essere usato al posto di quasi tutte le chiamate Getxxx in **ID3DXBaseEffect**.<br/> |
| [**GetVector**](id3dxbaseeffect--getvector.md)                                           | Ottiene un vettore.<br/>                                                                                                                                                                                                         |
| [**GetVectorArray**](id3dxbaseeffect--getvectorarray.md)                                 | Ottiene una matrice di vettori.<br/>                                                                                                                                                                                              |
| [**GetVertexShader**](id3dxbaseeffect--getvertexshader.md)                               | Ottiene un vertex shader.<br/>                                                                                                                                                                                                  |
| [**SetArrayRange**](id3dxbaseeffect--setarrayrange.md)                                   | Impostare l'intervallo di una matrice da passare al dispositivo.<br/>                                                                                                                                                                       |
| [**SetBool**](id3dxbaseeffect--setbool.md)                                               | Imposta un valore BOOL.<br/>                                                                                                                                                                                                     |
| [**SetBoolArray**](id3dxbaseeffect--setboolarray.md)                                     | Imposta una matrice di valori booleani.<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | Imposta un valore a virgola mobile.<br/>                                                                                                                                                                                           |
| [**SetFloatArray**](id3dxbaseeffect--setfloatarray.md)                                   | Imposta una matrice di valori a virgola mobile.<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | Imposta un numero intero.<br/>                                                                                                                                                                                                       |
| [**SetIntArray**](id3dxbaseeffect--setintarray.md)                                       | Imposta una matrice di numeri interi.<br/>                                                                                                                                                                                             |
| [**SetMatrix**](id3dxbaseeffect--setmatrix.md)                                           | Imposta una matrice non trasposta.<br/>                                                                                                                                                                                          |
| [**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)                                 | Imposta una matrice di matrici non trasposte.<br/>                                                                                                                                                                               |
| [**SetMatrixPointerArray**](id3dxbaseeffect--setmatrixpointerarray.md)                   | Imposta una matrice di puntatori a matrici non trasposte.<br/>                                                                                                                                                                   |
| [**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)                         | Imposta una matrice trasposta.<br/>                                                                                                                                                                                              |
| [**SetMatrixTransposeArray**](id3dxbaseeffect--setmatrixtransposearray.md)               | Imposta una matrice di matrici trasposte.<br/>                                                                                                                                                                                  |
| [**SetMatrixTransposePointerArray**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | Imposta una matrice di puntatori a matrici trasposte.<br/>                                                                                                                                                                      |
| [**Setstring**](id3dxbaseeffect--setstring.md)                                           | Imposta una stringa.<br/>                                                                                                                                                                                                         |
| [**SetTexture**](id3dxbaseeffect--settexture.md)                                         | Imposta una trama.<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | Impostare il valore di un parametro o di un'annotazione arbitraria, inclusi tipi semplici, struct, matrici, stringhe, shader e trame. <br/>                                                                                        |
| [**SetVector**](id3dxbaseeffect--setvector.md)                                           | Imposta un vettore.<br/>                                                                                                                                                                                                         |
| [**SetVectorArray**](id3dxbaseeffect--setvectorarray.md)                                 | Imposta una matrice di vettori.<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXBASEEFFECT è definito come un puntatore a questa interfaccia.


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
