---
description: Il messaggio ADDRESSSTATE della linea TAPI \_ viene inviato quando lo stato di un indirizzo viene modificato in una riga attualmente aperta dall'applicazione. L'applicazione può richiamare lineGetAddressStatus per determinare lo stato corrente dell'indirizzo.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Messaggio di LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326744"
---
# <a name="line_addressstate-message"></a>\_Messaggio linea ADDRESSSTATE

Il messaggio **\_ ADDRESSSTATE della linea** TAPI viene inviato quando lo stato di un indirizzo viene modificato in una riga attualmente aperta dall'applicazione. L'applicazione può richiamare [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) per determinare lo stato corrente dell'indirizzo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per il dispositivo della linea.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore dell'indirizzo che ha modificato lo stato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Stato dell'indirizzo modificato. Può essere una o più delle [**\_ costanti LINEADDRESSSTATE**](lineaddressstate--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ ADDRESSSTATE** viene inviato a qualsiasi applicazione che ha aperto il dispositivo a linee e che ha abilitato questo messaggio. L'invio di questo messaggio per i vari elementi di stato può essere controllato e sottoposto a query usando [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) e [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Per impostazione predefinita, la creazione di report sullo stato degli indirizzi è disabilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




