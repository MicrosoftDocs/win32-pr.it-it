---
title: Simbolo D3D12SDKVersion
description: Numero di versione di Direct3D 12 SDK.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: 0bf0aa17e16a4274b69e80580c0615ed055dd97a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917922"
---
# <a name="d3d12sdkversion-symbol"></a>Simbolo D3D12SDKVersion

Numero di versione di Direct3D 12 SDK.

## <a name="syntax"></a>Sintassi

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Valore restituito

UINT [contenente](/windows/win32/winprog/windows-data-types) il numero di versione di Direct3D 12 SDK.

## <a name="remarks"></a>Commenti

**D3D12SDKVersion** non è associato a una libreria di importazione né a un file di intestazione.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | N/A |
| **Libreria** | N/A |
| **DLL** | d3d12core.dll |

## <a name="see-also"></a>Vedere anche
