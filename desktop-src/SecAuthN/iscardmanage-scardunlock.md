---
description: Rilascia l'uso esclusivo del smart card.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: Metodo ISCardManage::SCardUnlock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1c100d1607cceea95264e9af24ba29b23824dee833c14e492cfb0a1dd7ad396f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013891"
---
# <a name="iscardmanagescardunlock-method"></a>Metodo ISCardManage::SCardUnlock

\[Il **metodo SCardUnlock** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo SCardUnlock** rilascia l'uso esclusivo del [*smart card*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disposizione* \[ Pollici\]
</dt> <dd>

Stato in cui lasciare il smart card quando viene rilasciato il blocco.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**Lasciare**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**UNPOWER**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**Espellere**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro Disposition* non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

Per bloccare l'smart card connessa, [**chiamare SCardLock**](iscardmanage-scardlock.md).

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

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
