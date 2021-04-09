---
description: Tipo di oggetto.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: Enumerazione D3DXPARAMETER_CLASS (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886269"
---
# <a name="d3dxparameter_class-enumeration"></a>\_Enumerazione della classe D3DXPARAMETER

Tipo di oggetto.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**\_Scalare D3DXPC**
</dt> <dd>

Constant è un valore scalare.

</dd> <dt>

<span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**\_Vettore D3DXPC**
</dt> <dd>

Constant è un vettore.

</dd> <dt>

<span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**\_Righe matrice \_ D3DXPC**
</dt> <dd>

Constant è una matrice principale della riga.

</dd> <dt>

<span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**\_Colonne della matrice D3DXPC \_**
</dt> <dd>

Constant è una matrice principale della colonna.

</dd> <dt>

<span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**\_Oggetto D3DXPC**
</dt> <dd>

Constant è una trama, uno shader o una stringa.

</dd> <dt>

<span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**\_Struct D3DXPC**
</dt> <dd>

Constant è una struttura.

</dd> <dt>

<span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ Force \_ DWORD**
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
</dt> <dt>

[**\_TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




