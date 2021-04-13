---
description: Definisce le costanti che descrivono la modalità di nebbia.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumerazione D3DFOGMODE (D3D9Types. h)
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
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355239"
---
# <a name="d3dfogmode-enumeration"></a>Enumerazione D3DFOGMODE

Definisce le costanti che descrivono la modalità di nebbia.

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

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ None**
</dt> <dd>

Nessun effetto di nebbia.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ Exp**
</dt> <dd>

L'effetto nebbia si intensifica in modo esponenziale in base alla formula seguente.

![formula dell'intensità dell'effetto nebbia](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**\_Exp2 D3DFOG**
</dt> <dd>

L'effetto nebbia si intensifica in modo esponenziale con il quadrato della distanza in base alla formula seguente.

![formula dell'intensità dell'effetto nebbia basata sul quadrato della distanza](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ lineare**
</dt> <dd>

L'effetto nebbia si intensifica in modo lineare tra i punti di inizio e di fine, in base alla formula seguente.

![formula dell'intensità dell'effetto nebbia in base ai punti iniziale e finale](images/fogliner.png)

Questa è l'unica modalità di nebbia attualmente supportata.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori in questo tipo enumerato vengono usati dagli Stati di \_ rendering D3DRS FOGTABLEMODE e D3DRS \_ FOGVERTEXMODE.

La nebbia può essere considerata una misura di visibilità: più basso è il valore di nebbia prodotto da un'equazione di nebbia, minore è la visibilità di un oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
