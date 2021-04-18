---
title: Funzione MpManagerStatusQueryEx (MpClient. h)
description: Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager. | Funzione MpManagerStatusQueryEx (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerStatusQueryEx
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321968"
---
# <a name="mpmanagerstatusqueryex-function"></a>MpManagerStatusQueryEx (funzione)

Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*dwFlag* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Controlla quali informazioni della query vengono restituite. Alcune informazioni sono costose e potrebbero non essere necessarie.



| Valore                                                                                                                                                                                                         | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**\_flag di \_ query stato MP \_ \_ nessuno**</dt> </dl>       | Valore predefinito.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**\_flag di \_ query stato MP \_ \_ nostate**</dt> </dl> | Non eseguire una query per ottenere informazioni sullo stato.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ out\]
</dt> <dd>

Tipo: **PMPSTATUS \_ info**

Puntatore a una struttura che restituisce informazioni sullo stato relative a Last scansioni, minacce attive e stato di vari componenti. Vedere [**MPSTATUS \_ info**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**. Questa chiamata di funzione ha esito positivo anche se un servizio antimalware non è in esecuzione.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito. Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_informazioni MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





