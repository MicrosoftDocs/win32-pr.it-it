---
description: "Metodo IRTC::GetControlState: il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione è in esecuzione o sospesa."
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: Metodo IRTC::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2e41ad3e4119fffbada26fe3ebebdfe3bf82043
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110709"
---
# <a name="irtcgetcontrolstate-method"></a>Metodo IRTC::GetControlState

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



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | NPP non è connesso alla rete. Chiamare [IRTC::Connect](irtc-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>  | NPP è connesso alla rete, ma non con il [metodo IRTC::Connect.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato ogni volta che il NPP è connesso alla rete. È possibile usare questo metodo per determinare se un'acquisizione è in esecuzione, se l'acquisizione è sospesa o se l'acquisizione è stata arrestata ma NPP è ancora connesso.

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

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




