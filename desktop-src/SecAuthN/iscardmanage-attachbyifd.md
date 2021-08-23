---
description: Crea un collegamento di comunicazione a un lettore, utilizzando un nome visualizzato fornito per il lettore.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: Metodo ISCardManage::AttachByIFD
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
ms.openlocfilehash: cfc95f8c4318dbc78e3cbd93faf18fd5e8e764ab251096cc0a2c321dedd00002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922866"
---
# <a name="iscardmanageattachbyifd-method"></a>Metodo ISCardManage::AttachByIFD

\[Il **metodo AttachByIFD** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo AttachByIFD** crea un collegamento di comunicazione a un [*lettore*](../secgloss/r-gly.md), utilizzando un nome visualizzato fornito per il lettore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrIFDName* \[ Pollici\]
</dt> <dd>

Nome visualizzato del lettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro bstrIFDName* non è valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                            |



 

## <a name="remarks"></a>Commenti

Per collegare un [*smart card*](../secgloss/s-gly.md) [**chiamare AttachByHandle**](iscardmanage-attachbyhandle.md).

Per rilasciare un allegato, chiamare [**Detach.**](iscardmanage-detach.md)

Per riconnettersi al smart card senza chiamare [**Detach**](iscardmanage-detach.md) e **AttachByIFD,** chiamare [**Reconnect**](iscardmanage-reconnect.md).

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

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Riconnetti**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
