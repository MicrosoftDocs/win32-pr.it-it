---
description: Il metodo put MediaTitle imposta un titolo testuale per il contenuto multimediale che l'applicazione può usare a \_ scopo informativo o di visualizzazione. Deve essere una stringa convertibile ASCII se il set di caratteri è ASCII. In caso contrario, può essere qualsiasi stringa BSTR.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: Metodo ITMedia::p ut_MediaTitle (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd07111cfa737be7ec5750a147ffd8d598e68b819f27f03a901a01fd66fbfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682751"
---
# <a name="itmediaput_mediatitle-method"></a>Metodo ITMedia::p ut \_ MediaTitle

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo put \_ MediaTitle** imposta un titolo testuale per il contenuto multimediale che l'applicazione può usare a scopo informativo o di visualizzazione. Deve essere una stringa convertibile ASCII se il set di caratteri è ASCII. In caso contrario, può essere qualsiasi **stringa BSTR.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaTitle* \[ Pollici\]
</dt> <dd>

Puntatore a **un oggetto BSTR** contenente il titolo del contenuto multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pMediaTitle* non è un puntatore valido.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro pMediaTitle* non è valido.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro pMediaTitle* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

Questa funzione può inviare dati in rete in formato non crittografato. Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati. Prima di utilizzare questo metodo, è necessario considerare il rischio di sicurezza dell'invio dei dati in testo non crittografato.

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

[**ITMedia::get \_ MediaTitle**](itmedia-get-mediatitle.md)
</dt> </dl>

 

