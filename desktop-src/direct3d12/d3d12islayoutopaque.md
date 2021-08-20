---
title: Funzione D3D12IsLayoutOpaque (D3dx12.h)
description: Indica se il layout è opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- Funzione D3D12IsLayoutOpaque
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db512ac96e4df41f3fc70d15cd8286a191cd56dd5e862d4061df4d69cd10ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098134"
---
# <a name="d3d12islayoutopaque-function"></a>Funzione D3D12IsLayoutOpaque

Indica se il layout è opaco.

## <a name="syntax"></a>Sintassi


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Layout* 
</dt> <dd>

Tipo: **[ **LAYOUT TRAMA \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

Layout da controllare, come [**LAYOUT TEXTURE \_ \_ D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Valore **bool** che indica se il layout è opaco. Un layout è opaco se è D3D12 TEXTURE LAYOUT UNKNOWN o \_ \_ \_ D3D12 \_ TEXTURE \_ LAYOUT \_ 64KB \_ \_ UNDEFINED SWIZZLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





