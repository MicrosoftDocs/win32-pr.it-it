---
description: Il metodo Configure Invia le informazioni di configurazione usate per un'acquisizione.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Metodo IDelaydCConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484316"
---
# <a name="idelaydcconfigure-method"></a>Metodo IDelaydC:: Configure

Il metodo **Configure** Invia le informazioni di configurazione usate per un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConfigurationBlob* \[ in\]
</dt> <dd>

Handle per il BLOB che contiene le informazioni di configurazione.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore. Per informazioni sul contenuto di un BLOB di errore, vedere la sezione Osservazioni in questo argomento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                      | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>                  | Il NPP segnala che la sessione di acquisizione è stata avviata.<br/>                          |
| <dl> <dt>**\_disco NMERR \_ non \_ \_ fisso locale**</dt> </dl>    |                                                                                           |
| <dl> <dt>**NMERR \_ non è in grado di \_ \_ creare \_ memoria**</dt> </dl> |                                                                                           |
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl>            | Memoria non disponibile. Arrestare Windows per liberare risorse.<br/>               |
| <dl> <dt>**\_parametro NMERR non valido \_**</dt> </dl>         | Il BLOB di configurazione specificato dal parametro hConfiguration non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato, arrestato, ma non disconnesso.

Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*. Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi. Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.

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

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




