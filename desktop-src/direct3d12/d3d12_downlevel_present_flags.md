---
title: Enumerazione D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Flag passati al metodo ID3D12CommandQueueDownlevel::P reinviate.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322181"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>\_ \_ Enumerazione flag presenti di livello inferiore D3D12 \_

Flag passati alla funzione [**ID3D12CommandQueueDownlevel::P reinviato**](id3d12commandqueuedownlevel-present.md) per modificare il comportamento.

## <a name="syntax"></a>Sintassi

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Costanti

**D3D12 \_ il \_ flag presente di livello inferiore \_ \_ None**

Non è stata selezionata alcuna opzione.

**Il \_ \_ flag presente D3D12 di livello inferiore \_ attende il \_ \_ \_ VBLANK**

L'operazione **corrente** non verrà eseguita fino a quando non si verifica un vsync dall'ultima volta in cui si **presenta** ed.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------|------------------|
| Intestazione | d3d12downlevel. h |
| DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vedi anche
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Enumerazioni Direct3D 12 su Windows 7](direct3d-12on7-enumerations.md)
* [Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 in Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
