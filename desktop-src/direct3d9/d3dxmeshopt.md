---
description: 'Enumerazione D3DXMESHOPT: specifica il tipo di ottimizzazione della mesh da eseguire.'
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Enumerazione D3DXMESHOPT (D3dx9mesh.h)
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
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114349"
---
# <a name="d3dxmeshopt-enumeration"></a>Enumerazione D3DXMESHOPT

Specifica il tipo di ottimizzazione della mesh da eseguire.

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

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ COMPACT**
</dt> <dd>

Riordina i visi per rimuovere i vertici e i visi inutilizzati.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**
</dt> <dd>

Riordina i visi per ottimizzare un minor numero di modifiche dello stato del bundle di attributi e migliorare le prestazioni [**di ID3DXBaseMesh::D rawSubset.**](id3dxbasemesh--drawsubset.md)

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**
</dt> <dd>

Riordina i visi per aumentare la frequenza di riscontri nella cache delle cache dei vertici.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**
</dt> <dd>

Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**
</dt> <dd>

Ottimizzare solo i visi; non ottimizzare i vertici.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**
</dt> <dd>

Durante l'ordinamento degli attributi, non dividere i vertici condivisi tra gruppi di attributi.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**DISPOSITIVO D3DXMESHOPTINDEPENDENT \_**
</dt> <dd>

Influisce sulle dimensioni della cache dei vertici. L'uso di questo flag specifica una dimensione predefinita della cache dei vertici che funziona correttamente nell'hardware legacy.

</dd> </dl>

## <a name="remarks"></a>Commenti

I flag di ottimizzazione D3DXMESHOPT \_ STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE si escludono a vicenda.

Il flag SHAREVB D3DXMESHOPT \_ è stato rimosso da questa enumerazione. In alternativa, usare D3DXMESH \_ VB \_ SHARE, in [**D3DXMESH.**](./d3dxmesh.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
