---
description: Descrive il percorso del file di inclusione.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: Enumerazione D3DXINCLUDE_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530895"
---
# <a name="d3dxinclude_type-enumeration"></a>\_Enumerazione del tipo D3DXINCLUDE

Descrive il percorso del file di inclusione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ locale**
</dt> <dd>

Cercare il file di inclusione nel progetto locale.

</dd> <dt>

<span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**\_Sistema D3DXINC**
</dt> <dd>

Esaminare il percorso di sistema per il file di inclusione.

</dd> <dt>

<span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




