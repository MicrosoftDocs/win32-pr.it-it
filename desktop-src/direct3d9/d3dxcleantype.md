---
description: Definisce le operazioni da eseguire sui vertici in preparazione alla pulizia della rete.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumerazione D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235061"
---
# <a name="d3dxcleantype-enumeration"></a>Enumerazione D3DXCLEANTYPE

Definisce le operazioni da eseguire sui vertici in preparazione alla pulizia della rete.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKfacing**
</dt> <dd>

Unisci triangoli che condividono gli stessi indici di vertice ma hanno normali facciali che puntano in direzioni opposte (triangoli rivolti verso il retro). A meno che i triangoli non vengano divisi aggiungendo un vertice replicato, i dati di adiacenza mesh dei due triangoli potrebbero essere in conflitto.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**\_BOWTIES D3DXCLEAN**
</dt> <dd>

Se un vertice è il vertice di due ventilatori a triangolo (bowtie) e le operazioni di mesh avranno effetto su una delle ventole, suddivideranno il vertice condiviso in due nuovi vertici. Bowties può causare problemi per le operazioni, ad esempio la semplificazione della rete che rimuove i vertici, perché la rimozione di un vertice interessa due set distinti di triangoli.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN \_ skining**
</dt> <dd>

Usare questo flag per impedire l'esecuzione di cicli infiniti durante la scuoiatura delle operazioni mesh di installazione.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**\_Ottimizzazione D3DXCLEAN**
</dt> <dd>

Usare questo flag per evitare cicli infiniti durante le operazioni di ottimizzazione della rete.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Semplificazione D3DXCLEAN**
</dt> <dd>

Usare questo flag per evitare cicli infiniti durante le operazioni di semplificazione della rete.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




