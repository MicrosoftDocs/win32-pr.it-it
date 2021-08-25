---
description: Definisce le operazioni da eseguire sui vertici in preparazione per la pulizia della mesh.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Enumerazione D3DXCLEANTYPE (D3dx9mesh.h)
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
ms.openlocfilehash: 2517c59d5505a8f2892ef0aee1d3884b8d489625637002d6e69a4f86434237fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894111"
---
# <a name="d3dxcleantype-enumeration"></a>Enumerazione D3DXCLEANTYPE

Definisce le operazioni da eseguire sui vertici in preparazione per la pulizia della mesh.

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

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_ BACKFACING**
</dt> <dd>

Unire triangoli che condividono gli stessi indici dei vertici, ma con normali della faccia che puntano in direzioni opposte (triangoli rivolti all'indietro). A meno che i triangoli non vengano suddivisi aggiungendo un vertice replicato, i dati di adizia della mesh dei due triangoli possono essere in conflitto.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**
</dt> <dd>

Se un vertice è il vertice di due ventole di triangolo (un arco) e le operazioni di mesh influiranno su una delle ventole, suddividere il vertice condiviso in due nuovi vertici. Le archi possono causare problemi per operazioni come la semplificazione della mesh che rimuovono i vertici, perché la rimozione di un vertice influisce su due set distinti di triangoli.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**INTERFACCIA D3DXCLEAN \_**
</dt> <dd>

Usare questo flag per evitare cicli infiniti durante le operazioni di configurazione della mesh di configurazione dell'interfaccia.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**OTTIMIZZAZIONE D3DXCLEAN \_**
</dt> <dd>

Usare questo flag per impedire cicli infiniti durante le operazioni di ottimizzazione della mesh.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**SEMPLIFICAZIONE D3DXCLEAN \_**
</dt> <dd>

Usare questo flag per evitare cicli infiniti durante le operazioni di semplificazione della mesh.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




