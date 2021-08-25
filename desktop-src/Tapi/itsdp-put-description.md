---
description: Il metodo put \_ Description imposta la descrizione della sessione.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: Metodo ITSdp::p ut_Description (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe47e55b41de2c656f04872846c8be9352c53a0f6265a27e0eefbb1ceb1d5d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873691"
---
# <a name="itsdpput_description-method"></a>Metodo ITSdp::p ut \_ Description

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo put \_ Description** imposta la descrizione della sessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDescription* \[ Pollici\]
</dt> <dd>

Puntatore a un **BSTR contenente** la descrizione della sessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pDescription* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve [**usare SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *pDescription* e [**usare SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

[**ITSdp**](itsdp.md)
</dt> <dt>

[**Descrizione di ITSdp::get \_**](itsdp-get-description.md)
</dt> </dl>

 

