---
description: Il metodo SetPhoneNumbers imposta una matrice di numeri di telefono associati a un BLOB di conferenze.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'Metodo ITSdp:: SetPhoneNumbers (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329325"
---
# <a name="itsdpsetphonenumbers-method"></a>Metodo ITSdp:: SetPhoneNumbers

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetPhoneNumbers** imposta una matrice di numeri di telefono associati a un BLOB di conferenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Numeri* \[ in\]
</dt> <dd>

SAFEARRAY di **BSTR** s che elenca i numeri di telefono.

</dd> <dt>

*Nomi* \[ di in\]
</dt> <dd>

SAFEARRAY dei nomi degli elenchi di **BSTR**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *numeri* o *nomi* non è valido.<br/>     |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Gli elenchi a cui puntano i *numeri* e i *nomi* sono della stessa lunghezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




