---
title: Funzione FreeSoHAttributeValue (NapUtil.h)
description: Libera una struttura di dati SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- Funzione FreeSoHAttributeValue NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877a333c7eb43c3921c7727bcc15a958bdcd2565fabe4636a67868f3a27bf473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940405"
---
# <a name="freesohattributevalue-function"></a>Funzione FreeSoHAttributeValue

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione FreeSoHAttributeValue** libera una [**struttura di dati SoHAttributeValue.**](sohattributevalue-union.md)

## <a name="syntax"></a>Sintassi


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Valore [**SoHAttributeType**](sohattributetype-enum.md) che specifica il tipo di valore dell'attributo SoH da liberare.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Puntatore a [**SoHAttributeValue**](sohattributevalue-union.md) da liberare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema nap usano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **In** i parametri vengono allocati e liberati dal chiamante.
-   **I** parametri out vengono allocati dal chiamato e liberati dal chiamante usando **CoTaskMem.**
-   **I parametri in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem.**

Tutte le funzioni di Protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





