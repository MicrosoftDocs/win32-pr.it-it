---
title: Funzione D3DPERF_QueryRepeatFrame
description: Determinare se un profiler delle prestazioni richiede che il frame corrente venga nuovamente inviato a Direct3D per l'analisi delle prestazioni. Questa funzione non è attualmente supportata da PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "103723878"
---
# <a name="d3dperf_queryrepeatframe-function"></a>Funzione D3DPERF_QueryRepeatFrame

Determinare se un profiler delle prestazioni richiede che il frame corrente venga nuovamente inviato a Direct3D per l'analisi delle prestazioni. Questa funzione non è attualmente supportata da PIX.

## <a name="syntax"></a>Sintassi

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>Valore restituito

Se il valore restituito è TRUE, il chiamante deve ripetere la stessa sequenza di chiamate. Se FALSE, il chiamante deve continuare.

## <a name="remarks"></a>Commenti

La funzione deve essere chiamata immediatamente dopo la chiamata di **IDirect3DDevice9::P** reinviate.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | d3d9. h |
| **Libreria** | d3d9. lib |
| **DLL** | d3d9.dll |