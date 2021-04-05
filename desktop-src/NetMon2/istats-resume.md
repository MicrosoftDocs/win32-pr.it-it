---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'Metodo IStats:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883665"
---
# <a name="istatsresume-method"></a>IStats:: Resume (metodo)

Il metodo **Resume** riavvia un'acquisizione sospesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                | Descrizione                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>       | L'oggetto NPP non è connesso alla rete.<br/>                                                                                          |
| <dl> <dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt> </dl> | L'acquisizione non è sospesa. Chiamare il metodo [IStats::P ause](istats-pause.md) per arrestare temporaneamente l'acquisizione.<br/>                     |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>       | L'oggetto NPP non è connesso alla rete. Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ \_ solo statistiche**</dt> </dl>     | L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono acquisiti fino a quando non viene chiamato il metodo IStats:: Resume per riavviare l'acquisizione.

Quando si utilizzano i metodi di **sospensione** e **ripresa** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.

Per arrestare l'acquisizione, chiamare [IStats:: Stop](istats-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats:: Stop](istats-stop.md)
</dt> </dl>

 

 




