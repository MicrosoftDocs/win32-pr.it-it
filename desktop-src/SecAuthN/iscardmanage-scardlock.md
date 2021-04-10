---
description: Blocca una smart card connessa per l'uso esclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Metodo ISCardManage:: SCardLock'
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
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226961"
---
# <a name="iscardmanagescardlock-method"></a>Metodo ISCardManage:: SCardLock

\[Il metodo **SCardLock** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **SCardLock** blocca una [*Smart Card*](../secgloss/s-gly.md) connessa per un uso esclusivo.

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
| <dl> <dt>**\_OK**</dt> </dl>   | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Non è stato possibile completare l'operazione.<br/>     |



 

## <a name="remarks"></a>Commenti

Per rilasciare l'utilizzo esclusivo della smart card connessa, chiamare [**SCardUnlock**](iscardmanage-scardunlock.md).

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

[**SCardUnlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
