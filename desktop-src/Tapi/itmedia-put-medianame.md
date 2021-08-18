---
description: Il metodo put \_ MediaName imposta il nome del supporto. I supporti definiti sono audio, video, lavagna, testo e dati.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: Metodo ITMedia::p ut_MediaName (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d77ffde28406b7fb527ed8679d1f65d6aba537e611b69d1ad31e8679f59fd0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003339"
---
# <a name="itmediaput_medianame-method"></a>Metodo ITMedia::p ut \_ MediaName

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo put \_ MediaName** imposta il nome del supporto. I supporti definiti sono audio, video, lavagna, testo e dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaName* \[ Pollici\]
</dt> <dd>

Puntatore a un **oggetto BSTR** contenente il nome del supporto da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pMediaName* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro pMediaName* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ MediaName**](itmedia-get-medianame.md)
</dt> </dl>

 

