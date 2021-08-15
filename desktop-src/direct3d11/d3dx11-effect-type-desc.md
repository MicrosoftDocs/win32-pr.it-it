---
title: D3DX11_EFFECT_TYPE_DESC (D3dx11effect.h)
description: Descrive un tipo di variabile di effetto.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC struttura Direct3D 11
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
ms.openlocfilehash: cc045b40105a698c9d051de791991c49d2b6d0dd4672d50f344e8781999dd5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989961"
---
# <a name="d3dx11_effect_type_desc-structure"></a>Struttura \_ \_ DESC D3DX11 EFFECT TYPE \_

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

**Typename**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome del tipo, ad esempio "float4" o "MyStruct".

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **CLASSE VARIABILE \_ SHADER \_ \_ D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

La classe variable (vedere [**D3D10 \_ SHADER \_ VARIABLE \_ CLASS).**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **TIPO DI VARIABILE \_ SHADER \_ \_ D3D10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

Tipo di variabile (vedere [**D3D10 \_ SHADER \_ VARIABLE \_ TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elementi**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi in questo tipo (0 se non è una matrice).

</dd> <dt>

**Members**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di membri (0 se non è una struttura).

</dd> <dt>

**prime righe**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di righe in questo tipo (0 se non è una primitiva numerica).

</dd> <dt>

**Colonne**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di colonne in questo tipo (0 se non è una primitiva numerica).

</dd> <dt>

**PackedSize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di byte necessari per rappresentare questo tipo di dati, se strettamente compresso.

</dd> <dt>

**Dimensioni decompresse**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di byte occupati da questo tipo di dati, quando disposti in un buffer costante.

</dd> <dt>

**Stride**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di byte da cercare tra gli elementi, se disposti in un buffer costante.

</dd> </dl>

## <a name="remarks"></a>Commenti

D3DX11 \_ EFFECT \_ TYPE \_ DESC viene usato con [ **ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Effetti 11 Strutture](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

