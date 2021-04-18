---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'Metodo IESP:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305873"
---
# <a name="iespresume-method"></a>Metodo IESP:: Resume

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



| Codice restituito                                                                                                | Descrizione                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt> </dl> | L'acquisizione non è sospesa. Chiamare [**IESP::P ause**](iesp-pause.md) per sospendere l'acquisizione.<br/>                        |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>       | L'oggetto NPP non è connesso alla rete. Chiamare [**IESP:: Connect**](iesp-connect.md) per connettersi alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>             | L'oggetto NPP è connesso alla rete, ma non con il metodo [**IESP:: Connect**](iesp-connect.md) .<br/>            |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato **IESP:: Resume** per riavviare l'acquisizione. Quando si utilizzano **pause** e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si usa **Sospendi** e **Riprendi** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.

Per arrestare l'acquisizione, chiamare [**IESP:: Stop**](iesp-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP:: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: Stop**](iesp-stop.md)
</dt> </dl>

 

 




