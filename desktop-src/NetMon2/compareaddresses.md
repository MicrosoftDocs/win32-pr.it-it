---
description: La funzione CompareAddresses Confronta due indirizzi, a indicare che uno degli indirizzi è maggiore di, minore o uguale all'altro indirizzo.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Funzione CompareAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314179"
---
# <a name="compareaddresses-function"></a>CompareAddresses (funzione)

La funzione **CompareAddresses** Confronta due indirizzi, a indicare che uno degli indirizzi è maggiore di, minore o uguale all'altro indirizzo.

## <a name="syntax"></a>Sintassi


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpAddress1* \[ in\]
</dt> <dd>

Puntatore al primo indirizzo.

</dd> <dt>

*lpAddress2* \[ in\]
</dt> <dd>

Puntatore al secondo indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se gli indirizzi sono uguali, la funzione restituisce zero.

Se il parametro *lpAddress1* specifica un indirizzo minore dell'indirizzo specificato dal parametro *lpAddress2* , il valore restituito è un numero negativo.

Se il parametro *lpAddress1* specifica un indirizzo maggiore dell'indirizzo specificato dal parametro *lpAddress2* , il valore restituito è un numero positivo.

## <a name="remarks"></a>Commenti

Un indirizzo minore di un altro indirizzo indica un frame precedente. Un indirizzo maggiore di un altro indirizzo indica un frame successivo.

In Network Monitor sono disponibili altre due funzioni, [CompareFrameDestAddress](compareframedestaddress.md) e [CompareFrameSourceAddress](compareframesourceaddress.md), che è possibile utilizzare per confrontare gli indirizzi. La funzione **CompareFrameDestAddress** confronta un determinato indirizzo con l'indirizzo di destinazione del frame e la funzione **CompareFrameSourceAddress** confronta un determinato indirizzo con l'indirizzo di origine del frame.

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




