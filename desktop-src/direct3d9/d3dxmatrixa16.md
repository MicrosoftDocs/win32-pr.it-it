---
description: Una matrice con allineamento a 16 byte 4x4 che contiene metodi e overload degli operatori.
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Struttura D3DXMATRIXA16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 57d2e5e796b929c87d4724d298758f26088918c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762005"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>Struttura D3DXMATRIXA16 (D3dx9math. h)

Una matrice con allineamento a 16 byte 4x4 che contiene metodi e overload degli operatori.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
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

Una matrice allineata a 16 byte, quando utilizzata dalle funzioni matematiche D3DX, è stata ottimizzata per migliorare le prestazioni sui processori Intel Pentium 4. Le matrici sono allineate indipendentemente dalla posizione in cui vengono create: nello stack di programmi, nell'heap o nell'ambito globale. L'allineamento viene eseguito usando \_ \_ declspec (align (16)), che funziona con Visual C++ .NET e con Visual C++ 6,0 solo quando è installato il pacchetto del processore. Sfortunatamente, non esiste alcun modo per rilevare il pacchetto del processore, quindi l'allineamento dei byte è attivato per impostazione predefinita solo con Visual C++ .NET.

I vettori e i quaternioni non sono allineati a byte in D3DX. Quando si usano i vettori e i quaternioni con le funzioni matematiche D3DX, usare \_ declspec (align (16)) per generare vettori e quaternioni allineati ai byte, in modo da offrire prestazioni migliori. La definizione di \_ declspec è illustrata di seguito.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Altri compilatori interpretano D3DXMATRIXA16 come D3DXMATRIX. L'utilizzo di questa struttura in un compilatore che non è effettivamente allineato alla matrice può risultare problematico perché non esporrà bug che ignorano l'allineamento. Se, ad esempio, un oggetto D3DXMATRIXA16 si trova all'interno di una struttura o di una classe, è possibile che una [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) venga eseguita con una compressione stretta (ignorando i limiti di 16 byte). Ciò causerebbe interruzioni di compilazione se il compilatore venisse a volte aggiunto allineando la matrice.

### <a name="d3dxmatrixa16"></a>D3DXMATRIXA16

**D3DXMATRIXA16** include le estensioni C++ seguenti.


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
