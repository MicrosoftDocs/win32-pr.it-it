---
description: Specifica il modo in cui viene ruotato il monitoraggio usato per visualizzare un'applicazione a schermo intero.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Enumerazione D3DDISPLAYROTATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322393"
---
# <a name="d3ddisplayrotation-enumeration"></a>Enumerazione D3DDISPLAYROTATION

Specifica il modo in cui viene ruotato il monitoraggio usato per visualizzare un'applicazione a schermo intero.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**Identità di D3DDISPLAYROTATION \_**
</dt> <dd>

La visualizzazione non viene ruotata.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

La visualizzazione è ruotata di 90 gradi.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

La visualizzazione è ruotata di 180 gradi.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

La visualizzazione è ruotata di 270 gradi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata in [**IDirect3D9Ex:: GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex:: GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)e [**IDirect3DSwapChain9Ex:: GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).

Le applicazioni possono scegliere di gestire autonomamente la rotazione del monitoraggio usando il [ \_ NOAUTOROTATE D3DPRESENTFLAG](d3dpresentflag.md), nel qual caso l'applicazione deve essere in grado di individuare il modo in cui viene ruotato il monitoraggio in modo che possa modificare di conseguenza il rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




