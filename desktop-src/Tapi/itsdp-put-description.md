---
description: Il \_ metodo Put Description imposta la descrizione della sessione.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: 'ITSdp: metodo:p ut_Description (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332821"
---
# <a name="itsdpput_description-method"></a>ITSdp::p \_ metodo di descrizione ut

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **put \_ Description** imposta la descrizione della sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDescription* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che contiene la descrizione della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pDescription* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PDescription* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

[**Descrizione di ITSdp:: Get \_**](itsdp-get-description.md)
</dt> </dl>

 

