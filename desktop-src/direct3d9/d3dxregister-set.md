---
description: Tipo di dati del registro.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: D3DXREGISTER_SET enumerazione (D3dx9shader.h)
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
ms.openlocfilehash: 5721009cac2632d1bac487615e765e9e3f9ad3ccdf50369ae3cc11630a915454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524576"
---
# <a name="d3dxregister_set-enumeration"></a>Enumerazione D3DXREGISTER \_ SET

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

<span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS \_ BOOL**
</dt> <dd>

.

</dd> <dt>

<span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**
</dt> <dd>

Numero intero 4D.

</dd> <dt>

<span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ FLOAT4**
</dt> <dd>

Numero a virgola mobile 4D.

</dd> <dt>

<span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS \_ SAMPLER**
</dt> <dd>

Il registro contiene i dati del campionatore 4D.

</dd> <dt>

<span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




