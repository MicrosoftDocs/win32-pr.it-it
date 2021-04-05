---
description: Crea un collegamento di comunicazione a una smart card (ICC) utilizzando un handle restituito dal gestore di risorse della smart card.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Metodo ISCardManage:: AttachByHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882657"
---
# <a name="iscardmanageattachbyhandle-method"></a>Metodo ISCardManage:: AttachByHandle

\[Il metodo **AttachByHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **AttachByHandle** crea un collegamento di comunicazione a una [*Smart Card*](../secgloss/s-gly.md) (ICC) utilizzando un handle restituito dal gestore di [*risorse*](../secgloss/r-gly.md)della smart card.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hICC* \[ in\]
</dt> <dd>

Handle per una smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *hICC* non è valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                     |



 

## <a name="remarks"></a>Commenti

Per alleghi una chiamata di [*Reader*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).

Per rilasciare una chiamata di allegato [**Disconnetti**](iscardmanage-detach.md).

Per riconnettersi con la smart card senza chiamare [**Detach**](iscardmanage-detach.md) e **AttachByHandle**, chiamare [**Reconnect**](iscardmanage-reconnect.md).

Per un elenco di tutti i metodi definiti dall'interfaccia [**ISCardManage**](iscardmanage.md) , vedere [**ISCardManage**](iscardmanage.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Scollegare**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Riconnetti**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
