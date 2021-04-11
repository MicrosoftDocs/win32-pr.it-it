---
description: Descrive un vettore a due componenti, inclusi gli overload degli operatori e i cast di tipo.
ms.assetid: 5b7b4847-b994-48c6-ae3c-e48ee1716ddd
title: Struttura D3DXVECTOR2 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 860c7ddaba61adcd93a38469117b2a95779240a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235122"
---
# <a name="d3dxvector2-structure-d3dx10mathh"></a>Struttura D3DXVECTOR2 (D3DX10Math. h)

Descrive un vettore a due componenti, inclusi gli overload degli operatori e i cast di tipo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a>Members

<dl> <dt>

**x**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente y.

</dd> </dl>

## <a name="remarks"></a>Commenti

**D3DXVECTOR2** include le estensioni C++ seguenti.

### <a name="d3dxvector2-extensions"></a>Estensioni D3DXVECTOR2


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
