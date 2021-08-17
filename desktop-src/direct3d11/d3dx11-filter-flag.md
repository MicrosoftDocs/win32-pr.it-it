---
title: D3DX11_FILTER_FLAG enumerazione (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Flag di filtro delle trame.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- D3DX11_FILTER_FLAG enumerazione Direct3D 11
- LPD3DX11_FILTER_FLAG puntatore di enumerazione Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02ddbf1785d1032ab28a990d022950b2f28acc4b032ecdc9a72d5704665c03b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537002"
---
# <a name="d3dx11_filter_flag-enumeration"></a>Enumerazione FILTER FLAG D3DX11 \_ \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Flag di filtro delle trame.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11 \_ FILTER \_ NONE**
</dt> <dd>

Non verrà fatto alcun ridimensionamento o filtro. Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano di colore nero trasparente.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**PUNTO DI FILTRO D3DX11 \_ \_**
</dt> <dd>

Ogni pixel di destinazione viene calcolato tramite il campionamento del pixel più vicino dall'immagine di origine.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ FILTER \_ LINEAR**
</dt> <dd>

Ogni pixel di destinazione viene calcolato tramite il campionamento dei quattro pixel più vicini dall'immagine di origine. Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**TRIANGOLO FILTRO D3DX11 \_ \_**
</dt> <dd>

Ogni pixel nell'immagine di origine contribuisce in modo uniforme all'immagine di destinazione. Questo è il più lento dei filtri.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**CASELLA FILTRO D3DX11 \_ \_**
</dt> <dd>

Ogni pixel viene calcolato mediamente da una casella di 2x2(x2) di pixel dall'immagine di origine. Questo filtro funziona solo quando le dimensioni della destinazione sono metà di quelle dell'origine, come nel caso delle mipmap.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ FILTER \_ MIRROR \_ U**
</dt> <dd>

I pixel al di fuori del bordo della trama sull'asse U devono essere speculari, non di cui è stato eseguito il wrapping.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11 \_ FILTER \_ MIRROR \_ V**
</dt> <dd>

I pixel al di fuori del bordo della trama sull'asse v devono essere speculari, senza eseguire il wrapping.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11 \_ FILTER \_ MIRROR \_ W**
</dt> <dd>

I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non di cui è stato eseguito il wrapping.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11 \_ FILTER \_ MIRROR**
</dt> <dd>

L'impostazione di questo flag è uguale a quando si specificano i flag D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V e \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**DITHERING FILTRO D3DX11 \_ \_**
</dt> <dd>

L'immagine risultante deve essere dithering usando un algoritmo dithering ordinato 4x4. Ciò si verifica quando si esegue la conversione da un formato a un altro.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**DIFFUSIONE DEL FILTRO D3DX11 \_ \_ \_**
</dt> <dd>

Eseguire il dithering diffuso sull'immagine quando si cambia da un formato a un altro.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ FILTER \_ SRGB \_ IN**
</dt> <dd>

I dati di input si trova nello spazio colore RGB (sRGB) standard. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ FILTER \_ SRGB \_ OUT**
</dt> <dd>

I dati di output si trova nello spazio colore RGB (sRGB) standard. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ FILTER \_ SRGB**
</dt> <dd>

Come specificare D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 esegue automaticamente la correzione gamma (per convertire i dati dei colori dallo spazio RGB allo spazio RGB standard) durante il caricamento dei dati di trama. Questa operazione viene eseguita automaticamente, ad esempio, quando i dati RGB vengono caricati da un file .png in una trama sRGB. Usare i flag di filtro SRGB per indicare se i dati non devono essere convertiti in spazio sRGB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





