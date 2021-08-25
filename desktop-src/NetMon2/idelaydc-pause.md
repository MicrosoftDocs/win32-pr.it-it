---
description: "Metodo IDelaydC::P ause: il metodo Pause sospende l'acquisizione corrente."
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Metodo IDelaydC::P ause (Netmon.h)
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
ms.openlocfilehash: dfe48afce1e8fd2350f1d1b696eb426a326ade1b30151e872afee30c0ed997f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910511"
---
# <a name="idelaydcpause-method"></a>Metodo IDelaydC::P ause

Il **metodo Pause** sospende l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl> | L'acquisizione è già in stato sospeso.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>  | Il NPP non acquisisce dati. Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>  | Il NPP non è connesso alla rete. Chiamare [IDelaydC::Connessione](idelaydc-connect.md) per connettere il NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>    | Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connessione.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è in pausa, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non viene chiamato il metodo **IDelaydC::Resume** per riavviare l'acquisizione. Quando **sospendi** **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si usa **IDelaydC::P ause** e **IDelaydC::Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione ogni volta che l'acquisizione è in esecuzione. [](c.md)

Per riavviare l'acquisizione, [chiamare IDelaydC::Resume](idelaydc-resume.md).

Per arrestare l'acquisizione, [chiamare IDelaydC::Stop](idelaydc-stop.md).

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

[IDelaydC::Connessione](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




