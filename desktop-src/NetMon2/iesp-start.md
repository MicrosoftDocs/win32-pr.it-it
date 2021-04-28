---
description: "Metodo IESP::Start: il metodo Start avvia un'acquisizione."
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: Metodo IESP::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd0d1159132e594b6d48ea6799da5846eeb626e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103799"
---
# <a name="iespstart-method"></a>Metodo IESP::Start

Il **metodo Start** avvia un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ Cambio\]
</dt> <dd>

Puntatore al nome del [*file di acquisizione*](c.md) usato per archiviare i dati di rete. Assicurarsi di memorizzare nella cache questo nome file, se necessario per riferimento futuro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl> | L'acquisizione viene sospesa e deve essere arrestata prima di poter essere riavviata. Chiamare [IESP::Stop per](iesp-stop.md) arrestare l'acquisizione.<br/> |
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>       | L'acquisizione è già stata avviata.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>  | NPP non è connesso alla rete. Chiamare [IESP::Connect](iesp-connect.md) per connettere NPP alla rete.<br/>          |
| <dl> <dt>**NMERR \_ NON \_ ESP**</dt> </dl>        | NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)<br/>                              |



 

## <a name="remarks"></a>Commenti

Il percorso del [*file di acquisizione*](c.md) è specificato nel Registro di sistema di Windows, ma è possibile usare Network Monitor per modificare il percorso della directory.

Quando si riavvia l'acquisizione usando i metodi IESP::Start e [IESP::Stop,](iesp-stop.md) è necessario chiamare il metodo [IESP::Configure](iesp-configure.md) per riconfigurare la connessione ogni volta che si chiama IESP::Start per riavviare l'acquisizione dei dati. Quando si avvia e si arresta l'acquisizione con questi tre metodi, viene creato un nuovo file di acquisizione a ogni avvio dell'acquisizione.

> [!Note]  
> È anche possibile avviare e arrestare l'acquisizione usando i metodi [IESP::P ause](iesp-pause.md) e [IESP::Resume.](iesp-resume.md) Quando vengono usati questi due metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.

 

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

[IESP::Configure](iesp-configure.md)
</dt> <dt>

[IESP::Connect](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP::Resume](iesp-resume.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




