---
description: Consente a un'applicazione di riconnettersi a un smart card o lettore senza dover eseguire rispettivamente una chiamata Detach seguita da una chiamata AttachByHandle o AttachByIFD.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: Metodo ISCardManage::Reconnect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9c0359a062f62e49b52b92623714e6d94aff015e53a71afa45d4a433c31f28c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013981"
---
# <a name="iscardmanagereconnect-method"></a>Metodo ISCardManage::Reconnect

\[Il **metodo Riconnetti** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Reconnect** consente a un'applicazione di riconnettersi a un [*smart card*](../secgloss/s-gly.md) o a un [*lettore*](../secgloss/r-gly.md) senza dover eseguire rispettivamente una chiamata [**Detach**](iscardmanage-detach.md) seguita da una chiamata [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD.**](iscardmanage-attachbyifd.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per associare un smart card [**chiamare AttachByHandle**](iscardmanage-attachbyhandle.md) [**o AttachByIFD**](iscardmanage-attachbyifd.md).

Per scollegare un smart card, chiamare [**Detach**](iscardmanage-detach.md).

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
