---
description: 'Struttura D3DXMATRIXA16 (D3dx9math.h): matrice allineata a 16 byte e 4x4 che contiene metodi e overload degli operatori.'
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Struttura D3DXMATRIXA16 (D3dx9math.h)
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
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094209"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>Struttura D3DXMATRIXA16 (D3dx9math.h)

Matrice allineata a 16 byte e 4x4 che contiene metodi e overload dell'operatore.

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

Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna. Ad esempio, \_ 34 indica lo stesso ₃₄ , il componente nella terza riga e nella quarta \[ \] colonna.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una matrice allineata a 16 byte, se usata dalle funzioni matematiche D3DX, è stata ottimizzata per migliorare le prestazioni nei processori Intel Pentium 4. Le matrici sono allineate indipendentemente dalla posizione in cui vengono create: nello stack di programmi, nell'heap o nell'ambito globale. L'allineamento viene ottenuto usando \_ \_ declspec(align(16)), che funziona con Visual C++ .NET e con Visual C++ 6.0 solo quando è installato il pacchetto del processore. Sfortunatamente, non è possibile rilevare il pacchetto del processore, quindi l'allineamento dei byte è attivato per impostazione predefinita solo con Visual C++ .NET.

I vettori e i quaternioni non sono allineati ai byte in D3DX. Quando si usano vettori e quaternioni con funzioni matematiche D3DX, usare \_ declspec(align(16)) per generare vettori e quaternioni allineati ai byte, perché le prestazioni saranno notevolmente migliori. La definizione \_ di declspec è illustrata qui.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Altri compilatori interpretano D3DXMATRIXA16 come D3DXMATRIX. L'uso di questa struttura in un compilatore che non allinea effettivamente la matrice può risultare problematico perché non espone bug che ignorano l'allineamento. Ad esempio, se un oggetto D3DXMATRIXA16 si trova all'interno di una struttura o di una classe, un [**oggetto memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) potrebbe essere eseguito con un pacchetto stretto (ignorando i limiti di 16 byte). Ciò causerebbe interruzioni di compilazione se il compilatore a volte aggiungesse l'allineamento della matrice.

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
| Intestazione<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
