---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'Metodo IRTC:: Resume (Netmon. h)'
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
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310499"
---
# <a name="irtcresume-method"></a>Metodo IRTC:: Resume

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



| Codice restituito                                                                                                | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt> </dl> | L'acquisizione non è sospesa. Chiamare [IRTC::P ause](irtc-pause.md) per sospendere l'acquisizione.<br/>                                |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>       | L'oggetto NPP non è connesso alla rete. Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non in \_ tempo reale**</dt> </dl>        | L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono acquisiti fino a quando una chiamata al metodo [IRTC:: Resume](idelaydc-resume.md) riavvia l'acquisizione.

Quando si utilizzano i metodi di **sospensione** e **ripresa** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.

Per arrestare l'acquisizione, chiamare il metodo [IRTC:: Stop](irtc-stop.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> </dl>

 

 




