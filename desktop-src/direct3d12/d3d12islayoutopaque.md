---
title: Funzione D3D12IsLayoutOpaque (D3dx12. h)
description: Indica se il layout è opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque (funzione)
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
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322177"
---
# <a name="d3d12islayoutopaque-function"></a>D3D12IsLayoutOpaque (funzione)

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

Tipo: **[ **\_ \_ layout trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

Layout da controllare come [**\_ \_ layout di trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Valore **booleano** che indica se il layout è opaco. Un layout è opaco se il layout di trama D3D12 è sconosciuto o il layout di \_ \_ \_ trama D3D12 64KB non è \_ \_ \_ \_ definito \_ SWIZZLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





