---
description: "Metodo IStats::Start: il metodo Start avvia un'acquisizione."
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: Metodo IStats::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 494ec12a0bb9c5c312f34e9cc53e82bfcbe155f90c38b98b2ba807e9c87b6945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037151"
---
# <a name="istatsstart-method"></a>Metodo IStats::Start

Il **metodo Start** avvia un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl>  | L'acquisizione è stata sospesa e deve essere arrestata prima di poter essere riavviata. Chiamare il [metodo IStats::Stop](istats-stop.md) per arrestare l'acquisizione.<br/> |
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>        | L'acquisizione è già stata avviata.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>   | Il NPP non è connesso alla rete. Chiamare il [metodo IStats::Connessione](istats-connect.md) per connettere il NPP alla rete.<br/>           |
| <dl> <dt>**NMERR \_ NON \_ SOLO \_ STATISTICHE**</dt> </dl> | Il NPP è connesso alla rete, ma non con il [metodo IStats::Connessione.](istats-connect.md)<br/>                                          |



 

## <a name="remarks"></a>Commenti

Quando si riavvia l'acquisizione usando i metodi IStats::Start e [IStats::Stop,](istats-stop.md) è necessario chiamare il metodo [IStats::Configure](istats-configure.md) per riconfigurare la connessione ogni volta che si chiama IStats::Start per riavviare Data Capture.

> [!Note]  
> È anche possibile avviare e arrestare l'acquisizione usando i metodi [IStats::P ause](istats-pause.md) [e IStats::Resume.](istats-resume.md) Quando si usano questi metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Connessione](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




