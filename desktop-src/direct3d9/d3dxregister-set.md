---
description: Tipo di dati del registro.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: Enumerazione D3DXREGISTER_SET (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322481"
---
# <a name="d3dxregister_set-enumeration"></a>\_Enumerazione set D3DXREGISTER

Tipo di dati del registro.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**\_Bool D3DXRS**
</dt> <dd>

.

</dd> <dt>

<span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**\_INT4 D3DXRS**
</dt> <dd>

numero intero 4D.

</dd> <dt>

<span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**\_Float4 D3DXRS**
</dt> <dd>

numero a virgola mobile 4D.

</dd> <dt>

<span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**\_Campionatore D3DXRS**
</dt> <dd>

Il registro contiene i dati del campionatore 4D.

</dd> <dt>

<span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ Force \_ DWORD**
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

[**\_CONSTANTINFO D3DXSHADER**](d3dxshader-constantinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




