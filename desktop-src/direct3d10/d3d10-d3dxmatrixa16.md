---
description: "Struttura D3DXMATRIXA16 (D3DX10Math.h): matrice 4x4 allineata a 16 byte che contiene metodi e overload dell'operatore."
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: Struttura D3DXMATRIXA16 (D3DX10Math.h)
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
- D3DX10Math.h
ms.openlocfilehash: e81071d44340ef7a4b874633e736e21016c697a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113189"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a>Struttura D3DXMATRIXA16 (D3DX10Math.h)

Matrice allineata a 4x4 a 16 byte che contiene metodi e overload dell'operatore.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Members

<dl> <dt>

**\_Ij**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna. Ad esempio, 34 indica lo stesso ₃₄ , il componente \_ nella terza riga e nella quarta \[ \] colonna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una matrice allineata a 16 byte, se usata dalle funzioni matematiche D3DX, è stata ottimizzata per migliorare le prestazioni nei processori Intel Pentium 4. Le matrici sono allineate indipendentemente dalla posizione in cui vengono create: nello stack di programmi, nell'heap o nell'ambito globale. L'allineamento viene ottenuto usando \_ \_ declspec(align(16)), che funziona con Visual C++ .NET e con Visual C++ 6.0 solo quando è installato il pacchetto del processore. Sfortunatamente, non è possibile rilevare il pacchetto del processore, quindi l'allineamento dei byte è attivato per impostazione predefinita solo con Visual C++ .NET.

I vettori e i quaternioni non sono allineati a byte in D3DX. Quando si usano vettori e quaternioni con funzioni matematiche D3DX, usare \_ declspec(align(16)) per generare vettori e quaternioni allineati ai byte, perché avranno prestazioni significativamente migliori. La definizione \_ di declspec è illustrata qui.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Altri compilatori **interpretano D3DXMATRIXA16** [**come D3DXMATRIX**](d3d10-d3dxmatrix.md). L'uso di questa struttura in un compilatore che non allinea effettivamente la matrice può essere problematico perché non esporrà bug che ignorano l'allineamento. Ad esempio, se un **oggetto D3DXMATRIXA16** si trova all'interno di una struttura o di una classe, è possibile che un [oggetto memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) venga eseguito con la creazione di un pacchetto stretto (ignorando i limiti a 16 byte). Ciò causerebbe interruzioni di compilazione se il compilatore aggiungesse a volte l'allineamento della matrice.

### <a name="d3dxmatrixa16-extensions"></a>Estensioni D3DXMATRIXA16

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
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
