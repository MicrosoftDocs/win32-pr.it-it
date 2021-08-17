---
description: Reimposta il contesto di sicurezza corrente dell'smart card.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: Metodo ISCardVerify::ResetSecurityState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6cf1d27298e5bc37288b209547e82f29cfba1393dc3c654563977fbd3f0bf0ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141064"
---
# <a name="iscardverifyresetsecuritystate-method"></a>Metodo ISCardVerify::ResetSecurityState

\[Il **metodo ResetSecurityState** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ResetSecurityState** reimposta il contesto [*di sicurezza corrente*](../secgloss/s-gly.md) dell'smart card . [](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetSecurityState();
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

Per abilitare nuovamente il contesto [*di sicurezza*](../secgloss/s-gly.md) senza reimpostazione, chiamare [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardVerify.**](iscardverify.md)

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

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[**Sbloccare**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))
</dt> </dl>

 

 
