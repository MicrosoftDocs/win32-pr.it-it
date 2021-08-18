---
description: Definisce il tipo di luce.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumerazione D3DLIGHTTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 66aefec5d614e5fc51f82741fbb30ace71222997273b7647c0bf51f2d5038878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804776"
---
# <a name="d3dlighttype-enumeration"></a>Enumerazione D3DLIGHTTYPE

Definisce il tipo di luce.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**PUNTO \_ D3DLIGHT**
</dt> <dd>

La luce è una fonte di punti. La luce ha una posizione nello spazio e emana luce in tutte le direzioni.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ SPOT**
</dt> <dd>

La luce è una fonte in evidenza. Questa luce è simile a una luce punto, ad eccezione del fatto che l'illuminazione è limitata a un cono. Questo tipo di luce ha una direzione e diversi altri parametri che determinano la forma del cono che produce. Per informazioni su questi parametri, vedere la [**struttura D3DLIGHT9.**](d3dlight9.md)

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ DIREZIONALE**
</dt> <dd>

La luce è una sorgente di luce direzionale. Equivale a usare una sorgente di luce punto a una distanza infinita.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le luci direzionali sono leggermente più veloci rispetto alle sorgenti di luce punto, ma hanno un aspetto leggermente migliore. I dati in evidenza offrono effetti visivi interessanti, ma richiedono molto tempo dal punto di vista computazionale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




