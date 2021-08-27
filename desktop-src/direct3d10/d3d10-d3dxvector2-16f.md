---
description: Descrive un vettore a due componenti che include gli overload degli operatori e i cast di tipo. Uguale a D3DXVECTOR2, ma usa valori a virgola mobile a 16 bit per x, y e z.
ms.assetid: b410d2e1-a006-4563-928a-c9000f73c224
title: D3DXVECTOR2_16F struttura (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e7d1c24b40674fe2df202a0cdea42dc7ad96728a8710c21e443642c8b6152cea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120261"
---
# <a name="d3dxvector2_16f-structure"></a>Struttura D3DXVECTOR2 \_ 16F

Descrive un vettore a due componenti che include gli overload degli operatori e i cast di tipo. Come [**D3DXVECTOR2,**](d3d10-d3dxvector2.md)ma usa valori a virgola mobile a 16 bit per x, y e z.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXVECTOR2_16F {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente y.

</dd> </dl>

## <a name="remarks"></a>Commenti

**D3DXVECTOR2 \_ 16F** include le estensioni C++ seguenti.

### <a name="d3dxvector2_16f-extensions"></a>Estensioni D3DXVECTOR2 \_ 16F


```

typedef struct D3DXVECTOR2_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR2_16F() {};
    D3DXVECTOR2_16F( CONST FLOAT * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR2_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR2_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y;

} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
