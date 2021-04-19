---
description: Il \_ metodo Get NumAddresses ottiene il numero di indirizzi da utilizzare per la sessione.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Metodo ITConnection:: get_NumAddresses (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326508"
---
# <a name="itconnectionget_numaddresses-method"></a>Metodo ITConnection:: Get \_ NumAddresses

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ NumAddresses** ottiene il numero di indirizzi da utilizzare per la sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Numero di indirizzi per la sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pNumAddresse* s non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




