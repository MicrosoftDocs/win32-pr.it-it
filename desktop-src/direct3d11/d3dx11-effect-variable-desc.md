---
title: Struttura D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Descrive una variabile di effetto.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- Struttura D3DX11_EFFECT_VARIABLE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996204"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>\_ \_ Struttura desc della variabile di effetto D3DX11 \_

Descrive una variabile di effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome della variabile, dell'annotazione o del membro della struttura.

</dd> <dt>

**Semantica**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Stringa semantica di questa variabile o membro della struttura (NULL per le annotazioni o se non è presente).

</dd> <dt>

**Flag**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flag facoltativi per le variabili di effetto.

</dd> <dt>

**annotazioni**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di annotazioni sulla variabile (sempre 0 per le annotazioni).

</dd> <dt>

**BufferOffset**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Offset in che contiene cbuffer o tbuffer (sempre 0 per le annotazioni o le variabili non nei buffer costanti).

</dd> <dt>

**ExplicitBindPoint**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Utilizzato se la variabile è stata associata in modo esplicito tramite la parola chiave register. Flag di controllo per \_ il \_ \_ punto di binding esplicito della variabile di effetto D3DX11 \_ \_ .

</dd> </dl>

## <a name="remarks"></a>Commenti

La \_ \_ variabile di effetto D3DX11 \_ desc viene usata con [**ID3DX11EffectVariable:: getdesc**](id3dx11effectvariable-getdesc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

