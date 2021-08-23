---
description: Il metodo SetPhoneNumbers imposta una matrice di numeri di telefono associati a un BLOB di conferenze.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: Metodo ITSdp::SetPhoneNumbers (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733dfbe4752281abf4063f308a05aec73203d361e3c9c5dcebf413eb4ba2af72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140214"
---
# <a name="itsdpsetphonenumbers-method"></a>Metodo ITSdp::SetPhoneNumbers

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo SetPhoneNumbers** imposta una matrice di numeri di telefono associati a un BLOB di conferenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Numeri* \[ Pollici\]
</dt> <dd>

SAFEARRAY di **BSTR che** elenca i numeri di telefono.

</dd> <dt>

*Nomi* \[ Pollici\]
</dt> <dd>

SAFEARRAY dei **nomi di elenco di BSTR.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Numbers* o *Names* non è valido.<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Gli elenchi a *cui puntano* *numeri* e nomi hanno la stessa lunghezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




