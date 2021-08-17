---
description: La funzione CompareFrameDestAddress confronta un indirizzo con l'indirizzo di destinazione di un frame.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Funzione CompareFrameDestAddress (Netmon.h)
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
ms.openlocfilehash: 153d1a5768791a33fd4f7629e071a125a4ee2ee46feaae366e2c1a21d8118f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367389"
---
# <a name="compareframedestaddress-function"></a>Funzione CompareFrameDestAddress

La **funzione CompareFrameDestAddress** confronta un indirizzo con l'indirizzo di destinazione di un frame.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per un frame.

</dd> <dt>

*lpAddress* \[ Pollici\]
</dt> <dd>

Puntatore a un indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se gli indirizzi sono uguali, il valore restituito è **TRUE.**

Se gli indirizzi non sono uguali, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Per la corretta restituzione della funzione **CompareFrameDestAddress,** il tipo di indirizzo di destinazione deve corrispondere al tipo di indirizzo specificato nel *parametro lpAddress.*

Network Monitor offre altre due funzioni, [CompareFrameSourceAddress](compareframesourceaddress.md) e [CompareAddresses,](compareaddresses.md)che è possibile usare per confrontare gli indirizzi. La **funzione CompareFrameSourceAddress** confronta un determinato indirizzo con l'indirizzo di origine del frame e la **funzione CompareAddress** confronta due indirizzi specificati.

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione CompareFrameDestAddress.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




