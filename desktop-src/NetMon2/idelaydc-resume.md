---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Metodo IDelaydC:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750058"
---
# <a name="idelaydcresume-method"></a>Metodo IDelaydC:: Resume

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



| Codice restituito                                                                                                | Descrizione                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt> </dl> | L'acquisizione non è sospesa. Chiamare [**IDelaydC::P ause**](idelaydc-pause.md) per sospendere l'acquisizione.<br/>                                |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>       | L'oggetto NPP non è connesso alla rete. Chiamare [**IDelaydC:: Connect**](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ ritardato**</dt> </dl>         | L'oggetto NPP è connesso alla rete, ma non con il metodo [**IDelaydC:: Connect**](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Commenti

Quando l'acquisizione viene sospesa, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato il metodo **IDelaydC:: Resume** per riavviare l'acquisizione. Quando si utilizzano [**pause**](idelaydc-pause.md) e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si usa [**Sospendi**](idelaydc-pause.md) e **Riprendi** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.

Per arrestare l'acquisizione, chiamare [**IDelaydC:: Stop**](idelaydc-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




