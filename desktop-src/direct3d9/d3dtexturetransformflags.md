---
description: Definisce i valori di trasformazione delle coordinate di trama.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumerazione D3DTEXTURETRANSFORMFLAGS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 514b8066b19ea5a3f558d9edee7cd57bae69dbb443e9b662a0209c9b57b58f31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096606"
---
# <a name="d3dtexturetransformflags-enumeration"></a>Enumerazione D3DTEXTURETRANSFORMFLAGS

Definisce i valori di trasformazione delle coordinate di trama.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ DISABLE**
</dt> <dd>

Le coordinate della trama vengono passate direttamente al rasterizzatore.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

Il rasterizzatore deve prevedere coordinate di trama 1D. Questo valore viene usato dall'elaborazione dei vertici di funzione fissa. Deve essere impostato su 0 quando si usa un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

Il rasterizzatore deve prevedere coordinate di trama 2D. Questo valore viene usato dall'elaborazione dei vertici di funzione fissa. Deve essere impostato su 0 quando si usa un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

Il rasterizzatore deve prevedere coordinate di trama 3D. Questo valore viene usato dall'elaborazione dei vertici di funzione fissa. Deve essere impostato su 0 quando si usa un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

Il rasterizzatore deve prevedere coordinate di trama 4D. Questo valore viene usato dall'elaborazione dei vertici di funzione fissa. Deve essere impostato su 0 quando si usa un vertex shader programmabile.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ PROIETTATO**
</dt> <dd>

Questo flag viene rispettato dalla pipeline di pixel a funzione fissa, nonché dalla pipeline di pixel programmabili nelle versioni da ps \_ \_ 1 1 a ps \_ 1 \_ 3. Quando la proiezione di trama è abilitata per una fase di trama, tutti e quattro i valori a virgola mobile devono essere scritti nel registro di trama corrispondente. Ogni coordinata di trama viene divisa per l'ultimo elemento prima di essere passata al rasterizzatore. Ad esempio, se questo flag viene specificato con il flag D3DTTFF COUNT3, la prima e la seconda coordinata della trama vengono divise per la terza coordinata prima di essere passate al \_ rasterizzatore.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le coordinate della trama possono essere trasformate usando una matrice 4 x 4 prima che i risultati vengono passati al rasterizzatore. Le trasformazioni delle coordinate di trama vengono impostate chiamando [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api)e passando lo stato della fase della trama TEXTURETRANSFORMFLAGS D3DTSS e uno dei valori di \_ **D3DTEXTURETRANSFORMFLAGS.** Per altre informazioni sulle trasformazioni di trama, vedere [Trasformazioni delle coordinate di trama (Direct3D 9).](texture-coordinate-transformations.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
