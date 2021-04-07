---
description: La funzione CompareFrameDestAddress confronta un indirizzo con l'indirizzo di destinazione di un frame.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Funzione CompareFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881441"
---
# <a name="compareframedestaddress-function"></a>CompareFrameDestAddress (funzione)

La funzione **CompareFrameDestAddress** confronta un indirizzo con l'indirizzo di destinazione di un frame.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per un frame.

</dd> <dt>

*lpAddress* \[ in\]
</dt> <dd>

Puntatore a un indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se gli indirizzi sono uguali, il valore restituito è **true**.

Se gli indirizzi non sono uguali, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Affinché la funzione **CompareFrameDestAddress** venga restituita correttamente, il tipo di indirizzo di destinazione deve corrispondere al tipo di indirizzo specificato nel parametro *lpAddress* .

In Network Monitor sono disponibili altre due funzioni, [CompareFrameSourceAddress](compareframesourceaddress.md) e [CompareAddresses](compareaddresses.md), che è possibile utilizzare per confrontare gli indirizzi. La funzione **CompareFrameSourceAddress** confronta un determinato indirizzo con l'indirizzo di origine del frame e la funzione **CompareAddress** Confronta due indirizzi specificati.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **CompareFrameDestAddress** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




