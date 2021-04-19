---
description: Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni del fotogramma chiave archiviato in un formato dati compresso.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interfaccia ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322831"
---
# <a name="id3dxcompressedanimationset-interface"></a>Interfaccia ID3DXCompressedAnimationSet

Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni del fotogramma chiave archiviato in un formato dati compresso.

## <a name="members"></a>Membri

L'interfaccia **ID3DXCompressedAnimationSet** eredita da [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXCompressedAnimationSet** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXCompressedAnimationSet** dispone di questi metodi.



| Metodo                                                                                  | Descrizione                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetCallbackKeys**](id3dxcompressedanimationset--getcallbackkeys.md)                 | Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.<br/>   |
| [**GetCompressedData**](id3dxcompressedanimationset--getcompresseddata.md)             | Ottiene il buffer di dati che archivia i dati di animazione del fotogramma chiave compressi.<br/> |
| [**GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | Ottiene il numero di chiavi di callback nel set di animazioni.<br/>                |
| [**GetPlaybackType**](id3dxcompressedanimationset--getplaybacktype.md)                 | Ottiene il tipo del ciclo di riproduzione del set di animazioni.<br/>                     |
| [**GetSourceTicksPerSecond**](id3dxcompressedanimationset--getsourcetickspersecond.md) | Ottiene il numero di cicli del fotogramma chiave di animazione che si verificano al secondo.<br/>   |



 

## <a name="remarks"></a>Commenti

Creare un set di animazioni con fotogrammi chiave in formato compresso con [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).

Il tipo LPD3DXCOMPRESSEDANIMATIONSET è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




