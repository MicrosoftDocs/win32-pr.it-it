---
description: Blocca un'istanza smart card per uso esclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: Metodo ISCardManage::SCardLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e610b914f1185eb2a1f4f7becdc8ba12c8aea4823630ecf3c5b9abe0f1ea3f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013941"
---
# <a name="iscardmanagescardlock-method"></a>Metodo ISCardManage::SCardLock

\[Il **metodo SCardLock** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo SCardLock** blocca un'istanza [*smart card*](../secgloss/s-gly.md) per uso esclusivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                            | Descrizione                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Impossibile completare l'operazione.<br/>     |



 

## <a name="remarks"></a>Commenti

Per rilasciare l'uso esclusivo del smart card connesso, chiamare [**SCardUnlock.**](iscardmanage-scardunlock.md)

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage.**](iscardmanage.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardUnlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
