---
description: Rilascia l'allegato a una smart card o un lettore specifico allocato rispettivamente da AttachByHandle e AttachByIFD.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage::D Metodo etach
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130654"
---
# <a name="iscardmanagedetach-method"></a>ISCardManage::D Metodo etach

\[Il metodo **Detach** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **Detach** rilascia l'allegato a una [*Smart Card*](../secgloss/s-gly.md) o a un [*lettore*](../secgloss/r-gly.md) specifico allocato rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) e [**AttachByIFD**](iscardmanage-attachbyifd.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Detach();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per connettere una smart card, chiamare [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md).

Per riconnettersi con la smart card senza chiamare **Detach** e [**AttachByHandle**](iscardmanage-attachbyhandle.md), chiamare [**Reconnect**](iscardmanage-reconnect.md).

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

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Riconnetti**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
