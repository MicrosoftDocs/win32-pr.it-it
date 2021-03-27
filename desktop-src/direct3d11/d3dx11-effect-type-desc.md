---
title: Struttura D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Descrive un tipo di variabile di effetto.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- Struttura D3DX11_EFFECT_TYPE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886318"
---
# <a name="d3dx11_effect_type_desc-structure"></a>\_ \_ Struttura Desc del tipo di effetto D3DX11 \_

Descrive un tipo di variabile di effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**TypeName**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome del tipo, ad esempio "float4" o "struct".

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **D3D10 \_ \_ \_ classe variabile shader**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

Classe della variabile (vedere [**la \_ classe della \_ variabile \_ shader D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **\_ \_ \_ tipo di variabile shader D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Tipo di variabile (vedere [**il \_ tipo di \_ variabile \_ shader D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elementi**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi in questo tipo (0 se non è una matrice).

</dd> <dt>

**Members**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di membri (0 se non è una struttura).

</dd> <dt>

**prime righe**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di righe in questo tipo (0 se non è una primitiva numerica).

</dd> <dt>

**Colonne**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di colonne in questo tipo (0 se non è una primitiva numerica).

</dd> <dt>

**PackedSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di byte necessari per rappresentare questo tipo di dati, quando è strettamente compresso.

</dd> <dt>

**UnpackedSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di byte occupati da questo tipo di dati, quando sono disposti in un buffer costante.

</dd> <dt>

**Stride**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di byte da cercare tra gli elementi, quando sono disposti in un buffer costante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il \_ \_ tipo di effetto D3DX11 \_ desc viene usato con [ **ID3DX11EffectType:: getdesc**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

