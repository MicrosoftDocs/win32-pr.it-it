---
description: Matrice 4x4 che contiene i metodi e gli overload degli operatori.
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: Struttura D3DXMATRIX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: cae887e2e9a8782cdc7ba159db203c929006c58a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323417"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a>Struttura D3DXMATRIX (D3DX10Math. h)

Matrice 4x4 che contiene i metodi e gli overload degli operatori.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a>Members

<dl> <dt>

**\_IJ**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna. 34, ad esempio, corrisponde \_ \[ a un ₄ ₃ \] , il componente nella terza riga e nella quarta colonna.

</dd> </dl>

## <a name="remarks"></a>Commenti

I programmatori C non possono utilizzare la struttura D3DXMATRIX, devono utilizzare la struttura D3DMATRIX. I programmatori C++ possono sfruttare i costruttori di overload e gli operatori di assegnazione, unario e binari (inclusi uguaglianza).

In D3DX, l' \_ elemento 34 di una matrice di proiezione non può essere un numero negativo. Se l'applicazione deve usare un valore negativo in questa posizione, deve ridimensionare l'intera matrice di proiezione di-1.

### <a name="d3dxmatrix-extensions"></a>Estensioni D3DXMATRIX

**D3DXMATRIX** include le estensioni C++ seguenti.


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
