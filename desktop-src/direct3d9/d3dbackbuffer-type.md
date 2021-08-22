---
description: Definisce costanti che descrivono il tipo di buffer nascosto.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: D3DBACKBUFFER_TYPE enumerazione (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: af8cc963f6b8f980b5cc1807cbbcf7ccb7e41249602eb96c683f69dd10180379
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279881"
---
# <a name="d3dbackbuffer_type-enumeration"></a>Enumerazione D3DBACKBUFFER \_ TYPE

Definisce costanti che descrivono il tipo di buffer nascosto.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER \_ TYPE \_ MONO**
</dt> <dd>

Specifica una catena di scambio nonstereo.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**TIPO D3DBACKBUFFER \_ \_ A SINISTRA**
</dt> <dd>

Specifica il lato sinistro di una coppia stereo in una catena di scambio.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**TIPO D3DBACKBUFFER \_ \_ RIGHT**
</dt> <dd>

Specifica il lato destro di una coppia stereo in una catena di scambio.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ TYPE \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Direct3D 9 non supporta la visualizzazione stereo, pertanto Direct3D non usa i valori D3DBACKBUFFER TYPE LEFT e \_ D3DBACKBUFFER TYPE RIGHT di questo tipo \_ \_ \_ enumerato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
