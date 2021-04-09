---
description: Definisce le costanti che descrivono le modalità di indirizzamento della trama supportate.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumerazione D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058594"
---
# <a name="d3dtextureaddress-enumeration"></a>Enumerazione D3DTEXTUREADDRESS

Definisce le costanti che descrivono le modalità di indirizzamento della trama supportate.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS a \_ capo**
</dt> <dd>

Affiancare la trama a ogni giunzione di interi. Ad esempio, per i valori compresi tra 0 e 3, la trama viene ripetuta tre volte. Nessun mirroring eseguito.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**\_Mirror D3DTADDRESS**
</dt> <dd>

Simile a D3DTADDRESS \_ wrap, ad eccezione del fatto che la trama viene capovolta a ogni giunzione di interi. per i valori compresi tra 0 e 1, ad esempio, la trama viene risolta normalmente; tra 1 e 2 la trama viene capovolta (con mirroring); da 2 a 3, la trama è di nuovo normale; E così via.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**\_Clamp D3DTADDRESS**
</dt> <dd>

Le coordinate di trama non comprese nell'intervallo \[ 0,0, 1,0 \] sono impostate rispettivamente sul colore della trama a 0,0 o 1,0.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Bordo D3DTADDRESS**
</dt> <dd>

Le coordinate di trama non comprese nell'intervallo \[ 0,0, 1,0 \] sono impostate sul colore del bordo.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**\_MIRRORONCE D3DTADDRESS**
</dt> <dd>

Simile a D3DTADDRESS \_ mirror e D3DTADDRESS \_ Clamp. Accetta il valore assoluto della coordinata di trama (pertanto, il mirroring circa 0) e quindi il morsetto al valore massimo. L'utilizzo più comune è per le trame del volume, in cui il supporto per la \_ modalità di indirizzamento della trama D3DTADDRESS MIRRORONCE completa non è necessario, ma i dati sono simmetrici intorno a un asse.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ Force \_ DWORD**
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
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
