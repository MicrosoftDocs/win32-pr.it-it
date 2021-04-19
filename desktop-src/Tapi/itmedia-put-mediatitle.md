---
description: Il \_ metodo Put MediaTitle imposta un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione. Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII. In caso contrario, può essere qualsiasi stringa BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: 'ITMedia: metodo:p ut_MediaTitle (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326238"
---
# <a name="itmediaput_mediatitle-method"></a>ITMedia::p UT \_ MediaTitle metodo

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **put \_ MediaTitle** imposta un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione. Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII. In caso contrario, può essere qualsiasi stringa **BSTR** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaTitle* \[ in\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il titolo del supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pMediaTitle* non è un puntatore valido.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pMediaTitle* non è valido.<br/>            |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PMediaTitle* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia:: Get \_ MediaTitle**](itmedia-get-mediatitle.md)
</dt> </dl>

 

