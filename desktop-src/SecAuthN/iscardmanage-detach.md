---
description: Rilascia l'allegato a un smart card o lettore allocato rispettivamente da AttachByHandle e AttachByIFD.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: Metodo ISCardManage::D etach
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
ms.openlocfilehash: 067c8e9f3e8cee607281d5f0a80ca813e91b425e63c15d3c1d47661acbbd04d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014091"
---
# <a name="iscardmanagedetach-method"></a>Metodo ISCardManage::D etach

\[Il **metodo Detach** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Detach** rilascia l'allegato a un smart card o lettore allocato rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) e [](../secgloss/s-gly.md) [**AttachByIFD.**](iscardmanage-attachbyifd.md) [](../secgloss/r-gly.md)

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
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per collegare un smart card [**chiamare AttachByHandle**](iscardmanage-attachbyhandle.md) [**o AttachByIFD.**](iscardmanage-attachbyifd.md)

Per riconnettersi al smart card senza chiamare **Detach** e [**AttachByHandle,**](iscardmanage-attachbyhandle.md)chiamare [**Reconnect**](iscardmanage-reconnect.md).

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

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Riconnetti**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
