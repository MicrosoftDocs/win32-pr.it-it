---
description: Il metodo pause sospende l'acquisizione corrente.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Metodo IDelaydC::P ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878638"
---
# <a name="idelaydcpause-method"></a>IDelaydC::P metodo ause

Il metodo **pause** sospende l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ sospesa**</dt> </dl> | L'acquisizione si trova già in uno stato di sospensione.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>  | L'oggetto NPP non sta acquisendo dati. Chiamare [IDelaydC:: Start](idelaydc-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>  | L'oggetto NPP non è connesso alla rete. Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ ritardato**</dt> </dl>    | L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato il metodo **IDelaydC:: Resume** per riavviare l'acquisizione. Quando si utilizzano **pause** e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si usa **IDelaydC::P ause** e **IDelaydC:: Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) ogni volta che viene eseguita l'acquisizione.

Per riavviare l'acquisizione, chiamare [IDelaydC:: Resume](idelaydc-resume.md).

Per arrestare l'acquisizione, chiamare [IDelaydC:: Stop](idelaydc-stop.md).

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

[IDelaydC:: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




