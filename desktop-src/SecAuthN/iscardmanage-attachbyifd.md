---
description: Crea un collegamento di comunicazione a un Reader, usando un nome visualizzato fornito per il lettore.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Metodo ISCardManage:: AttachByIFD'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313731"
---
# <a name="iscardmanageattachbyifd-method"></a>Metodo ISCardManage:: AttachByIFD

\[Il metodo **AttachByIFD** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **AttachByIFD** crea un collegamento di comunicazione a un [*Reader*](../secgloss/r-gly.md), usando un nome visualizzato fornito per il lettore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrIFDName* \[ in\]
</dt> <dd>

Nome visualizzato del lettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *bstrIFDName* non è valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                            |



 

## <a name="remarks"></a>Commenti

Per alleghi una [*Smart Card*](../secgloss/s-gly.md) , chiamare [**AttachByHandle**](iscardmanage-attachbyhandle.md).

Per rilasciare una chiamata di allegato [**Disconnetti**](iscardmanage-detach.md).

Per riconnettersi con la smart card senza chiamare [**Detach**](iscardmanage-detach.md) e **AttachByIFD**, chiamare [**Reconnect**](iscardmanage-reconnect.md).

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

[**Scollegare**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Riconnetti**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
