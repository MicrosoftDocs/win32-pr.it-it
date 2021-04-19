---
description: Il \_ metodo Put MachineAddress imposta l'indirizzo del computer dell'host di origine.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'ITSdp: metodo:p ut_MachineAddress (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332726"
---
# <a name="itsdpput_machineaddress-method"></a>ITSdp::p UT \_ MachineAddress metodo

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **put \_ MachineAddress** imposta l'indirizzo del computer dell'host di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMachineAddress* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che contiene l'indirizzo del computer dell'host della conferenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pMachineAddress* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>    |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                     |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PMachineAddress* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

Il parametro *pMachineAddress* può essere un nome DNS ("johnsmith.workinghard.Microsoft.com") o un indirizzo IP ("10.111.222.111").

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

[**ITSdp:: Get \_ MachineAddress**](itsdp-get-machineaddress.md)
</dt> </dl>

 

