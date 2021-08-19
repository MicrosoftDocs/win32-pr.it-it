---
description: Percentuale di tempo di elaborazione dei dati nel driver. Queste statistiche possono aiutare a identificare i casi in cui il driver è in attesa di altre risorse.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS struttura (D3D9Types.h)
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
ms.openlocfilehash: d7261096ed373620b8438ccce2d353ccf21f1c236028e8c829951fc64ee3725a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989031"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>Struttura D3DDEVINFO \_ D3D9INTERFACETIMINGS

Percentuale di tempo di elaborazione dei dati nel driver. Queste statistiche possono aiutare a identificare i casi in cui il driver è in attesa di altre risorse.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver in attesa del completamento della GPU con una risorsa bloccata (e [D3DLOCK \_ DONOTWAIT](d3dlock.md) non è stato specificato).

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver in attesa del completamento dell'elaborazione di alcuni comandi da parte della GPU prima che il driver possa inviare altri comandi. Ciò indica che il driver non ha più spazio per inviare comandi alla GPU.

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver in attesa che la latenza della GPU si riduca a meno di tre fotogrammi di rendering.

Se un'applicazione è limitata alla GPU, il driver deve bloccare la CPU fino a quando la GPU non si trova entro tre fotogrammi. In questo modo si impedisce a un'applicazione di eseguire l'accodamento di chiamate di rendering per molti secondi, il che può aumentare notevolmente la latenza tra quando l'utente esegue l'input di nuovi dati e quando l'utente vede i risultati di tale input. In generale, il driver può tenere traccia del numero di volte in cui viene chiamato [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per impedire l'accodamento di più di tre fotogrammi di lavoro di rendering.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver in attesa di una risorsa che non può essere pipelineta (gestita in parallelo). Un'applicazione potrebbe voler evitare di usare una risorsa non in pipeline per motivi di prestazioni.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato dal driver in attesa di altre elaborazioni GPU.

</dd> </dl>

## <a name="remarks"></a>Commenti

Queste metriche consentono di identificare quando un driver è in attesa e cosa è in attesa. Le percentuali elevate non sono necessariamente un problema.

Queste metriche globali del sistema possono essere implementate o meno. A seconda dell'hardware specifico, queste metriche potrebbero non supportare più query contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
