---
description: Il \_ metodo Put SessionVersion imposta la versione della sessione.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: 'ITSdp: metodo:p ut_SessionVersion (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332820"
---
# <a name="itsdpput_sessionversion-method"></a>ITSdp::p UT \_ SessionVersion metodo

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **put \_ SessionVersion** imposta la versione della sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SessionVersion* \[ in\]
</dt> <dd>

Valore della versione della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *SessionVersion* non è valido.<br/>         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Il valore restituito di questo metodo potrebbe essere **ULONG**, ma Visual Basic non supporta il tipo **ULONG** . Un **Double** è il tipo più piccolo successivo che comprende l'intero intervallo di valori necessari.

Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati. Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.

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
</dt> <dt>

[**ITSdp:: Get \_ SessionVersion**](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




