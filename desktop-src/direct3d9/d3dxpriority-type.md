---
description: Definisce il tipo di priorità a cui viene assegnata una traccia di animazione.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: D3DXPRIORITY_TYPE enumerazione (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: e7ea5b7447b896c6b582280216af4d6c05cc540286ad31a2bfb337975fe6c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524850"
---
# <a name="d3dxpriority_type-enumeration"></a>Enumerazione D3DXPRIORITY \_ TYPE

Definisce il tipo di priorità a cui viene assegnata una traccia di animazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ LOW**
</dt> <dd>

Il tracciato deve essere misto con tutte le tracce con priorità bassa prima che la combinazione con priorità bassa venga mista alla combinazione con priorità alta.

</dd> <dt>

<span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ HIGH**
</dt> <dd>

Le tracce devono essere combinate con tutte le tracce con priorità alta prima che la combinazione con priorità alta venga mista con la combinazione con priorità bassa.

</dd> <dt>

<span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le tracce con la stessa priorità vengono combinate tra loro e i due valori risultanti vengono quindi sfusi usando il fattore di blend di priorità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




