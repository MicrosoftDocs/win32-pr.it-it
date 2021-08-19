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
ms.openlocfilehash: bf3f4b70f1b06f5f985d459af361dc27f320d84465f5ef86f2d956339bf90ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778791"
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

Indicatore che l'acquisizione corrente è in esecuzione, incluso se l'acquisizione è sospesa.

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
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete. Chiamare [IRTC::Connessione](irtc-connect.md) per connettere il NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>  | Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connessione.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato ogni volta che il NPP è connesso alla rete. È possibile usare questo metodo per scoprire se un'acquisizione è in esecuzione, se l'acquisizione è sospesa o se l'acquisizione è stata arrestata ma il NPP è ancora connesso.

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

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




