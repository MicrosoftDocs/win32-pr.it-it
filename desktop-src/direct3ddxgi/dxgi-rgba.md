---
description: 'DXGI_RGBA struttura : rappresenta un valore di colore con alfa, usato per la trasparenza.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA struttura (DXGItype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114269"
---
# <a name="dxgi_rgba-structure"></a>Struttura DXGI \_ RGBA

Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a>Members

<dl> <dt>

**r**
</dt> <dd>

Valore a virgola mobile che specifica il componente rosso di un colore. Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0. Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il rosso è completamente presente.

</dd> <dt>

**G**
</dt> <dd>

Valore a virgola mobile che specifica il componente verde di un colore. Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0. Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.

</dd> <dt>

**b**
</dt> <dd>

Valore a virgola mobile che specifica il componente blu di un colore. Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0. Il valore 0,0 indica l'assenza completa del componente blu, mentre un valore pari a 1,0 indica che il blu è completamente presente.

</dd> <dt>

**Un**
</dt> <dd>

Valore a virgola mobile che specifica il componente alfa di un colore. Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0. Un valore pari a 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica che è completamente opaco.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile impostare i membri di questa struttura su valori esterni all'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti. I valori maggiori di 1 producono luci forti che tendono a evase una scena. I valori negativi producono luci scure che rimuovono effettivamente la luce da una scena.

L'intestazione DXGItype.h type definisce **DXGI \_ RGBA** come alias [**di D3DCOLORVALUE,**](d3dcolorvalue.md)come indicato di seguito:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



È possibile usare **DXGI \_ RGBA** [**con IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 e l'aggiornamento della piattaforma per le app desktop di Windows 7 \[ \| app UWP\]<br/>                        |
| Server minimo supportato<br/> | Windows Server 2012 e l'aggiornamento della piattaforma per le app desktop di Windows Server 2008 R2 \[ \| app UWP\]<br/> |
| Intestazione<br/>                   | <dl> <dt>DXGItype.h</dt> </dl>                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (in Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
