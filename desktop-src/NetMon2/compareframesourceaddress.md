---
description: La funzione CompareFrameSourceAddress confronta un indirizzo con l'indirizzo di origine di un frame.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Funzione CompareFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232843"
---
# <a name="compareframesourceaddress-function"></a>CompareFrameSourceAddress (funzione)

La funzione **CompareFrameSourceAddress** confronta un indirizzo con l'indirizzo di origine di un frame.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CompareFrameSourceAddress(
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

Affinché la funzione **CompareFrameSourceAddress** abbia esito positivo, il tipo di indirizzo di origine deve corrispondere al tipo di indirizzo specificato nel parametro *lpAddress* .

Network Monitor offre altre due funzioni per il confronto di indirizzi: [CompareFrameDestAddress](compareframedestaddress.md) e [CompareAddresses](compareaddresses.md). La funzione **CompareFrameDestAddress** confronta un determinato indirizzo con l'indirizzo di destinazione del frame e la funzione **CompareAddress** Confronta due indirizzi specificati.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **CompareFrameSourceAddress** .

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> </dl>

 

 




