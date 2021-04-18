---
description: Percentuale del tempo di elaborazione dei dati nel driver. Queste statistiche possono aiutare a identificare i casi in cui il driver è in attesa di altre risorse.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Struttura D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322406"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>\_Struttura D3DDEVINFO D3D9INTERFACETIMINGS

Percentuale del tempo di elaborazione dei dati nel driver. Queste statistiche possono aiutare a identificare i casi in cui il driver è in attesa di altre risorse.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver per attendere il completamento della GPU utilizzando una risorsa bloccata (e [D3DLOCK \_ DONOTWAIT](d3dlock.md) non è stato specificato).

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver per attendere che la GPU completi l'elaborazione di alcuni comandi prima che il driver possa inviare altro. Indica che il driver ha esaurito lo spazio necessario per inviare comandi alla GPU.

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver in attesa della latenza GPU per ridurre a meno di tre fotogrammi di rendering.

Se un'applicazione è limitata a GPU, il driver deve bloccare la CPU fino a quando la GPU non si trova all'interno di tre frame. In questo modo si impedisce a un'applicazione di accodare più secondi il numero di chiamate di rendering che possono aumentare significativamente la latenza tra il momento in cui l'utente immette nuovi dati e quando l'utente Visualizza i risultati di tale input. In generale, il [**driver è in**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) grado di tenere traccia del numero di volte in cui viene chiamato il metodo per impedire l'accodamento di più di tre frame del lavoro di rendering.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver per l'attesa di una risorsa che non può essere pipelineta (gestita in parallelo). Un'applicazione potrebbe voler evitare di usare una risorsa non pipeline per motivi di prestazioni.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver per l'attesa dell'elaborazione di altre GPU.

</dd> </dl>

## <a name="remarks"></a>Commenti

Queste metriche consentono di identificare il momento in cui un driver è in attesa e ciò che è in attesa. Le percentuali elevate non rappresentano necessariamente un problema.

Queste metriche globali del sistema possono essere implementate o meno. A seconda dell'hardware specifico, è possibile che queste metriche non supportino più query contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
