---
description: "Metodo IESP::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: Metodo IESP::Resume (Netmon.h)
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
ms.openlocfilehash: dd39cb83c90c566f0022679e70680e916daeb2a43a4d62e993e096930ee2f14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890471"
---
# <a name="iespresume-method"></a>Metodo IESP::Resume

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



| Codice restituito                                                                                                | Descrizione                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt> </dl> | L'acquisizione non viene sospesa. Chiamare [**IESP::P ause per**](iesp-pause.md) sospendere l'acquisizione.<br/>                        |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>       | NPP non è connesso alla rete. Chiamare [**IESP::Connessione**](iesp-connect.md) per connettersi alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ ESP**</dt> </dl>             | NPP è connesso alla rete, ma non con il metodo [**IESP::Connessione.**](iesp-connect.md)<br/>            |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è in stato di sospensione, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non viene chiamato **IESP::Resume** per riavviare l'acquisizione. Quando **sospendi** **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si **usano Pause** e **Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente. [](c.md)

Per arrestare l'acquisizione, chiamare [**IESP::Stop**](iesp-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP::Connessione**](iesp-connect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP::Stop**](iesp-stop.md)
</dt> </dl>

 

 




