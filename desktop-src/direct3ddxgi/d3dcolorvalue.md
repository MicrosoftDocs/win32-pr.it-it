---
description: Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Struttura D3DCOLORVALUE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354759"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>Struttura D3DCOLORVALUE (Dxgitype. h)

Rappresenta un valore di colore con alfa, utilizzato per la trasparenza.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
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

Il tipo di intestazione DXGItype. h definisce [**DXGI \_ RGBA**](dxgi-rgba.md) come alias di **D3DCOLORVALUE**, come indicato di seguito:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



È possibile usare D3DCOLORVALUE o [**DXGI \_ RGBA**](dxgi-rgba.md) con la modalità [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)e [**DXGI \_ Alpha \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**\_RGBA DXGI**](dxgi-rgba.md)
</dt> </dl>

 

 




