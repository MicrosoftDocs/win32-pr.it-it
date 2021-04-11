---
description: Rilascia l'utilizzo esclusivo della smart card connessa.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Metodo ISCardManage:: SCardUnlock'
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
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226959"
---
# <a name="iscardmanagescardunlock-method"></a>Metodo ISCardManage:: SCardUnlock

\[Il metodo **SCardUnlock** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **SCardUnlock** rilascia l'utilizzo esclusivo della [*Smart Card*](../secgloss/s-gly.md)connessa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disposizione* \[ in\]
</dt> <dd>

Stato in cui lasciare la smart card al rilascio del blocco.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**LASCIARE**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**Non alimentato**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**EJECT**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *Disposition* non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

Per bloccare la smart card connessa, chiamare [**SCardLock**](iscardmanage-scardlock.md).

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
