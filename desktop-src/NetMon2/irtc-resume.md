---
description: "Metodo IRTC::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: Metodo IRTC::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f8b8cebaf14f5e6a42a938a8fe585934137a899f8afaeb2d28533c0c0cfa18b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742981"
---
# <a name="irtcresume-method"></a>Metodo IRTC::Resume

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



| Codice restituito                                                                                                | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt> </dl> | L'acquisizione non viene sospesa. Chiamare [IRTC::P ause per](irtc-pause.md) sospendere l'acquisizione.<br/>                                |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>       | Il NPP non è connesso alla rete. Chiamare [IRTC::Connessione](irtc-connect.md) per connettere il protocollo NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>        | Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connessione.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è in stato di sospensione, i nuovi dati non vengono acquisiti fino a quando una chiamata al metodo [IRTC::Resume](idelaydc-resume.md) non riavvia l'acquisizione.

Quando si usano **i metodi Pause** **e Resume** per [](c.md) controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente.

Per arrestare l'acquisizione, chiamare [il metodo IRTC::Stop.](irtc-stop.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connessione](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




