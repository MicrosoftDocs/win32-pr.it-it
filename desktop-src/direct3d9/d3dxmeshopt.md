---
description: Specifica il tipo di ottimizzazione mesh da eseguire.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumerazione D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7d4f9f4ae36cec74ea86fcb50a194ac66d0add7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322630"
---
# <a name="d3dxmeshopt-enumeration"></a>Enumerazione D3DXMESHOPT

Specifica il tipo di ottimizzazione mesh da eseguire.

## <a name="syntax"></a>Sintassi


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**
</dt> <dd>

Riordina i visi per rimuovere i vertici e i visi inutilizzati.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**\_ATTRSORT D3DXMESHOPT**
</dt> <dd>

Riordina i visi per ottimizzare il minor numero di modifiche di stato del bundle di attributi e [**ID3DXBaseMesh avanzata::D rawsubset**](id3dxbasemesh--drawsubset.md) prestazioni.

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**\_VERTEXCACHE D3DXMESHOPT**
</dt> <dd>

Riordina i visi per aumentare la percentuale di riscontri nella cache delle cache dei vertici.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**\_STRIPREORDER D3DXMESHOPT**
</dt> <dd>

Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**\_IGNOREVERTS D3DXMESHOPT**
</dt> <dd>

Ottimizza solo le facce; non ottimizzare i vertici.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**\_DONOTSPLIT D3DXMESHOPT**
</dt> <dd>

Durante l'ordinamento degli attributi, non suddividere i vertici condivisi tra gruppi di attributi.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**\_DEVICEINDEPENDENT D3DXMESHOPT**
</dt> <dd>

Influiscono sulle dimensioni della cache dei vertici. L'uso di questo flag specifica una dimensione predefinita della cache Vertex che funziona correttamente nell'hardware legacy.

</dd> </dl>

## <a name="remarks"></a>Commenti

I \_ flag di ottimizzazione D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE si escludono a vicenda.

Il \_ flag SHAREVB di D3DXMESHOPT è stato rimosso da questa enumerazione. Usare \_ invece D3DXMESH VB \_ share, in [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
