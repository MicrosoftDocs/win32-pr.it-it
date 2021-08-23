---
description: Il metodo put \_ MachineAddress imposta l'indirizzo del computer dell'host di origine.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: Metodo ITSdp::p ut_MachineAddress (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974286e846268686423d0ebdbbd083d07e9946401cb0192713b200b2354b89c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060799"
---
# <a name="itsdpput_machineaddress-method"></a>Metodo ITSdp::p ut \_ MachineAddress

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo put \_ MachineAddress** imposta l'indirizzo del computer dell'host di origine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMachineAddress* \[ Pollici\]
</dt> <dd>

Puntatore a un **BSTR contenente** l'indirizzo del computer dell'host della conferenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pMachineAddress* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                     |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro pMachineAddress* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

Il *parametro pMachineAddress* può essere un nome DNS ("JohnSmith.workinghard.microsoft.com") o un indirizzo IP ("10.111.222.111").

Questa funzione può inviare dati in modalità non crittografata. Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati. Prima di usare questo metodo, è consigliabile considerare il rischio di sicurezza di inviare i dati in testo non crittografato.

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
</dt> <dt>

[**ITSdp::get \_ MachineAddress**](itsdp-get-machineaddress.md)
</dt> </dl>

 

