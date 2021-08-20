---
title: Funzione FreeNetworkSoH (NapUtil.h)
description: Libera una struttura di dati NetworkSoH.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- Funzione FreeNetworkSoH nap
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c2d3db800860295e0fa6173422ffeec0ca144550cc3ddfdf8a1ea391b6c6eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134752"
---
# <a name="freenetworksoh-function"></a>Funzione FreeNetworkSoH

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione FreeNetworkSoH** libera una struttura di dati [**NetworkSoH.**](/windows/win32/api/naptypes/ns-naptypes-networksoh)

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*networkSoh* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura di dati NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) da liberare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema nap usano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **I** parametri in vengono allocati e liberati dal chiamante.
-   **I** parametri out vengono allocati dal chiamato e liberati dal chiamante usando **CoTaskMem**.
-   **I parametri in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.

Tutte le funzioni di Protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





