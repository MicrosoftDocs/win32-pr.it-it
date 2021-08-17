---
description: Il metodo Start avvia l'acquisizione.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: Metodo IRTC::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 17ccb07a97112cab4390dc1eece2bf6fce51acf1c80244ed03253b5a2f6112b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132920"
---
# <a name="irtcstart-method"></a>Metodo IRTC::Start

Il **metodo Start** avvia l'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl> | L'acquisizione è in stato di sospensione e deve essere arrestata prima di poter essere riavviata. Chiamare [IRTC::Stop per](idelaydc-stop.md) arrestare l'acquisizione.<br/> |
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>       | L'acquisizione è già stata avviata.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>  | Il NPP non è connesso alla rete. Chiamare [IRTC::Connessione](irtc-connect.md) per connettere il NPP alla rete.<br/>                         |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>   | Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connessione.](irtc-connect.md)<br/>                                             |



 

## <a name="remarks"></a>Commenti

Quando si riavvia l'acquisizione usando i metodi IRTC::Start e [IRTC::Stop,](irtc-stop.md) è necessario chiamare il metodo [IRTC::Configure](irtc-configure.md) per riconfigurare la connessione ogni volta che si chiama IRTC::Start per riavviare Data Capture.

> [!Note]  
> È anche possibile avviare e arrestare l'acquisizione usando i metodi [IRTC::P ause](irtc-pause.md) [e IRTC::Resume.](irtc-resume.md)

 

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

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Connessione](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




