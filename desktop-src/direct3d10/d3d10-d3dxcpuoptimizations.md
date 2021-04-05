---
description: Abilita o Disabilita le ottimizzazioni della CPU.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Funzione D3DXCpuOptimizations (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762202"
---
# <a name="d3dxcpuoptimizations-function"></a>D3DXCpuOptimizations (funzione)

Abilita o Disabilita le ottimizzazioni della CPU.

## <a name="syntax"></a>Sintassi


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilita* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

**True** per abilitare le ottimizzazioni della CPU; in caso contrario, **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **\_ \_ Ottimizzazione CPU D3DX**](d3dx-cpu-optimization.md)**

Restituisce il tipo di CPU rilevato e per il quale sono disponibili le ottimizzazioni (vedere [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
