---
description: Opzioni per la saldatura dei vertici.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumerazione D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355039"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>Enumerazione D3DXWELDEPSILONSFLAGS

Opzioni per la saldatura dei vertici.

## <a name="syntax"></a>Sintassi


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**\_WELDALL D3DXWELDEPSILONS**
</dt> <dd>

Unire tutti i vertici presenti nella stessa posizione. L'uso di questo flag evita un confronto Epsilon tra i componenti dei vertici.

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**\_WELDPARTIALMATCHES D3DXWELDEPSILONS**
</dt> <dd>

Se un componente Vertex specificato si trova all'interno di Epsilon, modificare i vertici parzialmente corrispondenti in modo che entrambi i componenti siano identici. Se tutti i componenti sono uguali, rimuovere uno dei vertici.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**\_DONOTREMOVEVERTICES D3DXWELDEPSILONS**
</dt> <dd>

Indica alla saldatura di consentire solo modifiche ai vertici e non alla rimozione. Questo flag è valido solo se \_ è impostato D3DXWELDEPSILONS WELDPARTIALMATCHES. È utile modificare i vertici in modo che siano uguali, ma non consentire la rimozione di vertici.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**\_DONOTSPLIT D3DXWELDEPSILONS**
</dt> <dd>

Indica alla saldatura di non suddividere i vertici presenti in gruppi di attributi distinti. Quando il metodo [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) viene chiamato con il \_ flag D3DXMESHOPT ATTRSORT, \_ verrà impostato anche il flag D3DXMESHOPT DONOTSPLIT. L'impostazione di questo flag può rallentare l'elaborazione dei vertici software.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 




