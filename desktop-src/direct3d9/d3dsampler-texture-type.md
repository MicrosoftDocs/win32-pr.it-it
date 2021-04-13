---
description: Definisce i tipi di trama del campionatore per i vertex shader.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Enumerazione D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 337e8b25a8ec8389a6252fb48582128c601730ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401930"
---
# <a name="d3dsampler_texture_type-enumeration"></a>Enumerazione del tipo di \_ trama D3DSAMPLER \_

Definisce i tipi di trama del campionatore per i vertex shader.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ sconosciuto**
</dt> <dd>

Valore non inizializzato. Il valore di questo elemento è 0 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Dichiarazione di una trama 2D. Il valore di questo elemento è 2 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cubo D3DSTT**
</dt> <dd>

Dichiarazione di una trama del cubo. Il valore di questo elemento è 3 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volume D3DSTT**
</dt> <dd>

Dichiarazione di una trama del volume. Il valore di questo elemento è 4 &lt; &lt; D3DSP \_ TEXTURETYPE \_ Shift.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




