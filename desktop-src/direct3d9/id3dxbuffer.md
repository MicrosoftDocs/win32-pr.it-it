---
description: L'interfaccia ID3DXBuffer viene usata come buffer di dati, archiviando informazioni su vertici, adienze e materiali durante le operazioni di ottimizzazione e caricamento della mesh.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interfaccia ID3DXBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cc69262949b9cc700f0a7c477bcfacb7dacd1fc51eb836ad76dfaa2fecb7358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121679"
---
# <a name="id3dxbuffer-interface"></a>Interfaccia ID3DXBuffer

L'interfaccia ID3DXBuffer viene usata come buffer di dati, archiviando informazioni su vertici, adienze e materiali durante le operazioni di ottimizzazione e caricamento della mesh. L'oggetto buffer viene usato per restituire dati di lunghezza arbitraria. Inoltre, gli oggetti buffer vengono usati per restituire il codice oggetto e i messaggi di errore nei metodi che assemblano vertex shader e pixel shader.

## <a name="members"></a>Membri

**L'interfaccia ID3DXBuffer** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXBuffer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXBuffer** include questi metodi.



| Metodo                                                    | Descrizione                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Recupera un puntatore ai dati nel buffer.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Recupera le dimensioni totali dei dati nel buffer.<br/> |



 

## <a name="remarks"></a>Commenti

**L'interfaccia ID3DXBuffer** viene ottenuta chiamando la [**funzione D3DXCreateBuffer.**](d3dxcreatebuffer.md)

Il tipo LPD3DXBUFFER è definito come puntatore **all'interfaccia ID3DXBuffer.**


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
