---
description: Specifica la modalità di rotazione del monitor usato per visualizzare un'applicazione a schermo intero.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Enumerazione D3DDISPLAYROTATION (D3d9types.h)
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
ms.openlocfilehash: 8defdc206e88750125d88c50e86484428c0dedbd7c18575e26504d7445cd3f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804938"
---
# <a name="d3ddisplayrotation-enumeration"></a>Enumerazione D3DDISPLAYROTATION

Specifica la modalità di rotazione del monitor usato per visualizzare un'applicazione a schermo intero.

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

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**IDENTITÀ D3DDISPLAYROTATION \_**
</dt> <dd>

La visualizzazione non viene ruotata.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

La visualizzazione viene ruotata di 90 gradi.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

La visualizzazione viene ruotata di 180 gradi.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

La visualizzazione viene ruotata di 270 gradi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata in [**IDirect3D9Ex::GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex::GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)e [**IDirect3DSwapChain9Ex::GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).

Le applicazioni possono scegliere di gestire la rotazione del monitoraggio usando [D3DPRESENTFLAG \_ NOAUTOROTATE.](d3dpresentflag.md)In questo caso, l'applicazione dovrà sapere come viene ruotato il monitoraggio in modo che possa regolare il rendering di conseguenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




