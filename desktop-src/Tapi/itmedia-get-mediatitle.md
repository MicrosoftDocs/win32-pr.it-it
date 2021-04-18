---
description: Il \_ metodo Get MediaTitle recupera un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione. Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII. In caso contrario, può essere qualsiasi stringa BSTR.
ms.assetid: c5567672-54f0-45d6-81d2-5a501a33c25f
title: 'Metodo ITMedia:: get_MediaTitle (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f2ec4bf16fc27c23277113ee13c8fe02f89c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327993"
---
# <a name="itmediaget_mediatitle-method"></a>Metodo ITMedia:: Get \_ MediaTitle

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ MediaTitle** recupera un titolo testuale per i supporti che l'applicazione può usare a scopo informativo o di visualizzazione. Se il set di caratteri è ASCII, deve essere una stringa convertibile ASCII. In caso contrario, può essere qualsiasi stringa **BSTR** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MediaTitle(
  [out] BSTR *ppMediaTitle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppMediaTitle* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che contiene il titolo del supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppMediaTitle* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppMediaTitle* .

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

[**ITMedia::P UT \_ MediaTitle**](itmedia-put-mediatitle.md)
</dt> </dl>

 

