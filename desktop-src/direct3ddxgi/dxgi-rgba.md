---
description: Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: Struttura DXGI_RGBA (DXGItype. h)
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
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746767"
---
# <a name="dxgi_rgba-structure"></a>\_Struttura DXGI RGBA

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

Valore a virgola mobile che specifica il componente rosso di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il colore rosso è completamente presente.

</dd> <dt>

**g**
</dt> <dd>

Valore a virgola mobile che specifica il componente verde di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.

</dd> <dt>

**b**
</dt> <dd>

Valore a virgola mobile che specifica il componente blu di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica l'assenza completa del componente blu, mentre il valore 1,0 indica che il blu è completamente presente.

</dd> <dt>

**un**
</dt> <dd>

Valore a virgola mobile che specifica il componente alfa di un colore. Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0. Il valore 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica una piena opacità.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile impostare i membri di questa struttura su valori non compresi nell'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti. I valori maggiori di 1 producono luci forti che tendono a pulire una scena. I valori negativi producono luci scure che effettivamente rimuovono la luce da una scena.

Il tipo di intestazione DXGItype. h definisce **DXGI \_ RGBA** come alias di [**D3DCOLORVALUE**](d3dcolorvalue.md), come indicato di seguito:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



È possibile usare **DXGI \_ RGBA** con la modalità [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ Alpha \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 e aggiornamento della piattaforma per le app desktop di Windows 7 \[ \| UWP\]<br/>                        |
| Server minimo supportato<br/> | Windows Server 2012 e aggiornamento della piattaforma per le app desktop di Windows Server 2008 R2 \[ \| UWP\]<br/> |
| Intestazione<br/>                   | <dl> <dt>DXGItype. h</dt> </dl>                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (in Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
