---
description: Definisce le costanti che descrivono la modalità di sospensione.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumerazione D3DFOGMODE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b94992d94779932301c271ca46dc7466344b40b68c62855d4c57bfe8b780a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791985"
---
# <a name="d3dfogmode-enumeration"></a>Enumerazione D3DFOGMODE

Definisce le costanti che descrivono la modalità di sospensione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ NONE**
</dt> <dd>

Nessun effetto collaterale.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ EXP**
</dt> <dd>

L'effetto dell'acqua si intensifica in modo esponenziale, in base alla formula seguente.

![formula dell'intensità effetto-effetto](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

L'effetto dell'effetto intensifica in modo esponenziale il quadrato della distanza, in base alla formula seguente.

![formula dell'intensità dell'effetto a effetto in base al quadrato di distanza](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**LINEARE D3DFOG \_**
</dt> <dd>

L'effetto dell'effetto intensifica in modo lineare tra i punti iniziale e finale, in base alla formula seguente.

![formula dell'intensità degli effetti in base ai punti di inizio e di fine](images/fogliner.png)

Questa è l'unica modalità attualmente supportata.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori in questo tipo enumerato vengono usati dagli stati di rendering D3DRS \_ ESEGUITABLEMODE e D3DRSBIEVERTEXMODE. \_

Può essere considerato una misura di visibilità: più basso è il valore dell'oggetto prodotto da un'equazione dell'equazione, minore è la visibilità di un oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
