---
description: L'interfaccia ID3DXConstantTable viene utilizzata per accedere alla tabella Constant. Questa tabella contiene le variabili utilizzate dagli shader e dagli effetti dei linguaggi di alto livello.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interfaccia ID3DXConstantTable (D3DX9Shader. h)
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
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322796"
---
# <a name="id3dxconstanttable-interface"></a>Interfaccia ID3DXConstantTable

L'interfaccia ID3DXConstantTable viene utilizzata per accedere alla tabella Constant. Questa tabella contiene le variabili utilizzate dagli shader e dagli effetti dei linguaggi di alto livello.

## <a name="members"></a>Membri

L'interfaccia **ID3DXConstantTable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXConstantTable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXConstantTable** dispone di questi metodi.



| Metodo                                                                                       | Descrizione                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Ottiene un puntatore al buffer che contiene la tabella delle costanti.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Ottiene le dimensioni del buffer della tabella delle costanti.<br/>                                                                             |
| [**Getcostante**](id3dxconstanttable--getconstant.md)                                       | Ottiene una costante cercando il relativo indice.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Ottiene una costante cercandone il nome.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Ottiene un puntatore a una matrice di descrizioni di costanti nella tabella delle costanti.<br/>                                              |
| [**Getconstantelement**](id3dxconstanttable--getconstantelement.md)                         | Ottiene una costante da una matrice di costanti. Una matrice è costituita da elementi.<br/>                                            |
| [**Getdesc**](id3dxconstanttable--getdesc.md)                                               | Ottiene una descrizione della tabella delle costanti.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Restituisce l'indice del campionatore.<br/>                                                                                              |
| [**DiBOOL**](id3dxconstanttable--setbool.md)                                               | Imposta un valore booleano.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Imposta una matrice di valori booleani.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Imposta le costanti sui rispettivi valori predefiniti. I valori predefiniti sono dichiarati nelle dichiarazioni di variabili nello shader.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Imposta un numero a virgola mobile.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Imposta una matrice di numeri a virgola mobile.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Imposta un valore integer.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Imposta una matrice di numeri interi.<br/>                                                                                              |
| [**Sematrix**](id3dxconstanttable--setmatrix.md)                                           | Imposta una matrice nontransposed.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Imposta una matrice di matrici nontransposed.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Imposta una matrice di puntatori alle matrici nontransposed.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Imposta una matrice trasposta.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Imposta una matrice di matrici trasposte.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Imposta una matrice di puntatori a matrici trasposte.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Imposta il contenuto del buffer sulla tabella delle costanti.<br/>                                                                  |
| [**Sevector**](id3dxconstanttable--setvector.md)                                           | Imposta un vettore 4D.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Imposta una matrice di vettori 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXCONSTANTTABLE è definito come puntatore all'interfaccia **ID3DXConstantTable** .


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
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

 

 
