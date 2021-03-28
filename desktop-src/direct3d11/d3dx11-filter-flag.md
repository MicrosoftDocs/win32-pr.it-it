---
title: Enumerazione D3DX11_FILTER_FLAG (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Flag di filtro della trama.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Enumerazione D3DX11_FILTER_FLAG Direct3D 11
- Puntatore di enumerazione LPD3DX11_FILTER_FLAG Direct3D 11
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
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982574"
---
# <a name="d3dx11_filter_flag-enumeration"></a>\_Enumerazione flag di filtro D3DX11 \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Flag di filtro della trama.

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

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**\_Filtro D3DX11 \_ None**
</dt> <dd>

Non verrà eseguita alcuna operazione di ridimensionamento o filtro. Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano neri trasparenti.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Punto di filtro D3DX11 \_**
</dt> <dd>

Ogni pixel di destinazione viene calcolato eseguendo il campionamento del pixel più vicino dall'immagine di origine.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_Filtro D3DX11 \_ lineare**
</dt> <dd>

Ogni pixel di destinazione viene calcolato eseguendo il campionamento dei quattro pixel più vicini dall'immagine di origine. Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triangolo filtro \_ D3DX11**
</dt> <dd>

Ogni pixel nell'immagine di origine contribuisce ugualmente all'immagine di destinazione. Questo è il più lento dei filtri.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Casella filtro \_ D3DX11**
</dt> <dd>

Ogni pixel viene calcolato calcolando la media di una casella 2x2 (X2) di pixel dall'immagine di origine. Questo filtro funziona solo quando le dimensioni della destinazione sono la metà di quelle dell'origine, come nel caso di mipmap.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ filtro \_ mirror \_ U**
</dt> <dd>

I pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non incapsulati.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**\_Mirror del filtro D3DX11 \_ \_ V**
</dt> <dd>

I pixel al di fuori del bordo della trama sull'asse v devono essere rispecchiati, non incapsulati.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_Mirror filtro \_ D3DX11 \_ W**
</dt> <dd>

I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non incapsulati.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Mirror del filtro D3DX11 \_**
</dt> <dd>

Specificare questo flag equivale a specificare i flag D3DX Filter \_ mirror \_ \_ U, D3DX \_ Filter \_ mirror \_ V e D3DX \_ Filter \_ mirror \_ W.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Dithering filtro D3DX11 \_**
</dt> <dd>

L'immagine risultante deve essere retinata usando un algoritmo di dithering ordinato 4x4. Questo errore si verifica quando si esegue la conversione da un formato a un altro.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_Diffusione del \_ dithering del filtro D3DX11 \_**
</dt> <dd>

Quando si passa da un formato a un altro, è necessario diffonderne l'immagine.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**\_Filtro D3DX11 \_ sRGB \_ in**
</dt> <dd>

I dati di input sono nello spazio colore RGB (sRGB) standard. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtro \_ sRGB in \_ uscita**
</dt> <dd>

I dati di output sono nello spazio colore RGB (sRGB) standard. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ Filter \_ sRGB**
</dt> <dd>

Equivale a specificare il \_ filtro \_ D3DX \_ sRGB \| nel \_ filtro \_ D3DX \_ . Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 esegue automaticamente la correzione gamma (per convertire i dati di colore dallo spazio RGB allo spazio RGB standard) quando si caricano i dati della trama. Questa operazione viene eseguita automaticamente ad esempio quando i dati RGB vengono caricati da un file con estensione png in una trama sRGB. Usare i flag di filtro SRGB per indicare se non è necessario convertire i dati nello spazio sRGB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





