---
description: "Metodo IStats::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: Metodo IStats::Resume (Netmon.h)
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
ms.openlocfilehash: 72c73107ea4bf4662d4251a7c9e06ed1844feca88cb0ce6700887e65f6f08021
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063821"
---
# <a name="istatsresume-method"></a>Metodo IStats::Resume

Il **metodo Resume** riavvia un'acquisizione sospesa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                | Descrizione                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>       | NPP non è connesso alla rete.<br/>                                                                                          |
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt> </dl> | L'acquisizione non viene sospesa. Chiamare il [metodo IStats::P ause](istats-pause.md) per arrestare temporaneamente l'acquisizione.<br/>                     |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>       | NPP non è connesso alla rete. Chiamare il [metodo IStats::Connessione](istats-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt> </dl>     | NPP è connesso alla rete, ma non con il [metodo IStats::Connessione.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è in stato di sospensione, i nuovi dati non vengono acquisiti fino a quando non viene chiamato il metodo IStats::Resume per riavviare l'acquisizione.

Quando si usano **i metodi Pause** **e Resume** per [](c.md) controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente.

Per arrestare l'acquisizione, chiamare [IStats::Stop](istats-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStat](istats.md)
</dt> <dt>

[IStats::Connessione](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




