---
description: L'interfaccia ID3DXConstantTable viene usata per accedere alla tabella costante. Questa tabella contiene le variabili usate dagli effetti e dagli shader del linguaggio di alto livello.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interfaccia ID3DXConstantTable (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ead9e594e79daf8bd43bf4125b857030482028f7128c8063196413d52c9a8b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675481"
---
# <a name="id3dxconstanttable-interface"></a>Interfaccia ID3DXConstantTable

L'interfaccia ID3DXConstantTable viene usata per accedere alla tabella costante. Questa tabella contiene le variabili usate dagli effetti e dagli shader del linguaggio di alto livello.

## <a name="members"></a>Membri

**L'interfaccia ID3DXConstantTable** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXConstantTable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXConstantTable** include questi metodi.



| Metodo                                                                                       | Descrizione                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Ottiene un puntatore al buffer che contiene la tabella costante.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Ottiene le dimensioni del buffer della tabella costante.<br/>                                                                             |
| [**GetConstant**](id3dxconstanttable--getconstant.md)                                       | Ottiene una costante cercandone l'indice.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Ottiene una costante cercandone il nome.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Ottiene un puntatore a una matrice di descrizioni costanti nella tabella delle costanti.<br/>                                              |
| [**GetConstantElement**](id3dxconstanttable--getconstantelement.md)                         | Ottiene una costante da una matrice di costanti. Una matrice è costituito da elementi .<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Ottiene una descrizione della tabella delle costanti.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Restituisce l'indice del campionatore.<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | Imposta un valore booleano.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Imposta una matrice di valori booleani.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Imposta le costanti sui valori predefiniti. I valori predefiniti vengono dichiarati nelle dichiarazioni di variabili nello shader.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Imposta un numero a virgola mobile.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Imposta una matrice di numeri a virgola mobile.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Imposta un valore intero.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Imposta una matrice di numeri interi.<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | Imposta una matrice non trasposta.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Imposta una matrice di matrici non trasposte.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Imposta una matrice di puntatori a matrici non trasposte.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Imposta una matrice trasposta.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Imposta una matrice di matrici trasposte.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Imposta una matrice di puntatori a matrici trasposte.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Imposta il contenuto del buffer sulla tabella costante.<br/>                                                                  |
| [**SetVector**](id3dxconstanttable--setvector.md)                                           | Imposta un vettore 4D.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Imposta una matrice di vettori 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXCONSTANTTABLE è definito come puntatore **all'interfaccia ID3DXConstantTable.**


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
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

 

 
