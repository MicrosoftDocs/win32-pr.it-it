---
description: Definisce se la modalità a mosaico corrente è discreta o continua.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumerazione D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886293"
---
# <a name="d3dpatchedgestyle-enumeration"></a>Enumerazione D3DPATCHEDGESTYLE

Definisce se la modalità a mosaico corrente è discreta o continua.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discreto**
</dt> <dd>

Stile del bordo discreto. In modalità discreta, è possibile specificare lo schema a mosaico float, ma verrà troncato in numeri interi.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ continuo**
</dt> <dd>

Stile bordo continuo. In modalità continua, lo schema a mosaico viene specificato come valori float che possono essere facilmente variati per ridurre gli artefatti "pop".

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che lo schema a mosaico continuo produce uno schema a mosaico completamente diverso da quello discreto per gli stessi valori a mosaico (questo è più evidente in modalità wireframe). Pertanto, 4,0 Continuous non è uguale a 4 discreto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




