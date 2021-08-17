---
description: Il metodo SetEmailNames imposta una matrice di indirizzi di posta elettronica associati al BLOB della conferenza.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: Metodo ITSdp::SetEmailNames (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23fa550c5750a3fad5d0b20ccdf2e032ed98c20a10b2f8e758ea7c9874e05a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140234"
---
# <a name="itsdpsetemailnames-method"></a>Metodo ITSdp::SetEmailNames

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo SetEmailNames** imposta una matrice di indirizzi di posta elettronica associati al BLOB della conferenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indirizzi* \[ Pollici\]
</dt> <dd>

SAFEARRAY di **BSTR** che elenca gli indirizzi di posta elettronica.

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
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro Addresses* o *Names* non è valido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Gli elenchi a *cui puntano* *indirizzi* e nomi hanno la stessa lunghezza.

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

 

 




