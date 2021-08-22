---
description: Definisce il tipo di modalità di ciclo del set di animazioni usate per la riproduzione.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: D3DXPLAYBACK_TYPE enumerazione (D3dx9anim.h)
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
ms.openlocfilehash: 642c3e1d49792016ea1d161352d4dda9fc1330aab544880e754659c735d1ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044789"
---
# <a name="d3dxplayback_type-enumeration"></a>Enumerazione D3DXPLAYBACK \_ TYPE

Definisce il tipo di modalità di ciclo del set di animazioni usate per la riproduzione.

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

<span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**CICLO D3DXPLAY \_**
</dt> <dd>

L'animazione si ripete all'infinito.

</dd> <dt>

<span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ UNA SOLA VOLTA**
</dt> <dd>

L'animazione viene riprodotta una sola volta e quindi si arresta nell'ultimo fotogramma.

</dd> <dt>

<span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ PINGPONG**
</dt> <dd>

L'animazione alterna all'infinito tra la riproduzione in avanti e la riproduzione all'indietro.

</dd> <dt>

<span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




