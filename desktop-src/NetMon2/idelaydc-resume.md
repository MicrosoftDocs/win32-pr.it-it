---
description: "Metodo IDelaydC::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: Metodo IDelaydC::Resume (Netmon.h)
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
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109189"
---
# <a name="idelaydcresume-method"></a>Metodo IDelaydC::Resume

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



| Codice restituito                                                                                                | Descrizione                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt> </dl> | L'acquisizione non viene sospesa. Chiamare [**IDelaydC::P ause**](idelaydc-pause.md) per sospendere l'acquisizione.<br/>                                |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>       | NPP non è connesso alla rete. Chiamare [**IDelaydC::Connect**](idelaydc-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>         | NPP è connesso alla rete, ma non con il [**metodo IDelaydC::Connect.**](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Durante la sospensione dell'acquisizione, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non viene chiamato il metodo **IDelaydC::Resume** per riavviare l'acquisizione. Quando [**sospendi**](idelaydc-pause.md) **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si [**usano Pause**](idelaydc-pause.md) e **Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente. [](c.md)

Per arrestare l'acquisizione, [**chiamare IDelaydC::Stop**](idelaydc-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC::Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




