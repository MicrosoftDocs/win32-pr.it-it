---
description: Tipo di dati per la gestione di un set di parametri effetti predefiniti.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Struttura D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354884"
---
# <a name="d3dxeffectinstance-structure"></a>Struttura D3DXEFFECTINSTANCE

Tipo di dati per la gestione di un set di parametri effetti predefiniti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>Members

<dl> <dt>

**pEffectFilename**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome del file di effetti.

</dd> <dt>

**NumDefaults**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di parametri predefiniti.

</dd> <dt>

**pDefaults**
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**

</dd> <dd>

Puntatore a una matrice di elementi [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , ognuno dei quali contiene un parametro Effect.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
