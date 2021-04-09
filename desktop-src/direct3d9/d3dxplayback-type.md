---
description: Definisce il tipo di modalità di ciclo del set di animazioni utilizzato per la riproduzione.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Enumerazione D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886277"
---
# <a name="d3dxplayback_type-enumeration"></a>\_Enumerazione del tipo D3DXPLAYBACK

Definisce il tipo di modalità di ciclo del set di animazioni utilizzato per la riproduzione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Ciclo D3DXPLAY**
</dt> <dd>

L'animazione si ripete all'infinito.

</dd> <dt>

<span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ una volta**
</dt> <dd>

L'animazione viene riprodotta una volta e quindi si interrompe sull'ultimo frame.

</dd> <dt>

<span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**\_Pingpong D3DXPLAY**
</dt> <dd>

L'animazione si alterna all'infinito tra la riproduzione in avanti e la riproduzione a ritroso.

</dd> <dt>

<span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




