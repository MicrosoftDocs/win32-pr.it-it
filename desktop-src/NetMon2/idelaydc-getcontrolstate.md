---
description: "Metodo IDelaydC::GetControlState: il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione è in esecuzione o sospesa."
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: Metodo IDelaydC::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 34302215cf0e773d7713f56233d38462071f1dde725a85478688cfb9ca2a4f45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365894"
---
# <a name="idelaydcgetcontrolstate-method"></a>Metodo IDelaydC::GetControlState

Il **metodo GetControlState** recupera lo stato dell'acquisizione , che indica se l'acquisizione è in esecuzione o sospesa. [](c.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsRunnning* \[ Cambio\]
</dt> <dd>

Indicatore che l'acquisizione corrente è in esecuzione, anche se l'acquisizione è sospesa.

</dd> <dt>

*IsPaused* \[ Cambio\]
</dt> <dd>

Indicatore che l'acquisizione corrente è sospesa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | NPP non è connesso alla rete. Chiamare [IDelaydC::Connessione](idelaydc-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>   | NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connessione.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato ogni volta che il NPP è connesso alla rete usando [l'interfaccia IDelaydC.](idelaydc.md) È possibile usare questo metodo per determinare se un'acquisizione è in esecuzione, se l'acquisizione è sospesa o se l'acquisizione è stata arrestata ma NPP non è disconnesso.

I metodi usati per avviare, sospendere e arrestare l'acquisizione sono elencati nell'elenco Vedere anche riportato di seguito.

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

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




