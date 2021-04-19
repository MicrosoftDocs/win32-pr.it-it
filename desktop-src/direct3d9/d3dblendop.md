---
description: Definisce le operazioni di Blend supportate. Per le definizioni dei termini, vedere la sezione Osservazioni.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Enumerazione D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322377"
---
# <a name="d3dblendop-enumeration"></a>Enumerazione D3DBLENDOP

Definisce le operazioni di Blend supportate. Per le definizioni dei termini, vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ aggiungere**
</dt> <dd>

Il risultato è la destinazione aggiunta all'origine. Risultato = origine + destinazione

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**\_Sottrazione D3DBLENDOP**
</dt> <dd>

Il risultato è la destinazione sottratta da all'origine. Risultato = origine-destinazione

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**\_REVSUBTRACT D3DBLENDOP**
</dt> <dd>

Il risultato è l'origine sottratta dalla destinazione. Risultato = destinazione-origine

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ min**
</dt> <dd>

Il risultato è il valore minimo dell'origine e della destinazione. Risultato = MIN (origine, destinazione)

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**
</dt> <dd>

Il risultato è il valore massimo dell'origine e della destinazione. Risultato = MAX (origine, destinazione)

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'origine, la destinazione e il risultato sono definiti come segue:



| Termine        | Tipo   | Descrizione                                                            |
|-------------|--------|------------------------------------------------------------------------|
| Source (Sorgente)      | Input  | Colore del pixel di origine prima dell'operazione.                        |
| Destination | Input  | Colore del pixel nel buffer di destinazione prima dell'operazione.     |
| Risultato      | Output | Valore restituito che rappresenta il colore sfumato risultante dall'operazione. |



 

Questo tipo enumerato definisce i valori utilizzati dagli Stati di rendering seguenti:

-   \_BLENDOP D3DRS
-   \_BLENDOPALPHA D3DRS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
