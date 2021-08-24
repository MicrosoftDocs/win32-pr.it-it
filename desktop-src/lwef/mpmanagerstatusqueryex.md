---
title: Funzione MpManagerStatusQueryEx (MpClient.h)
description: Restituisce informazioni sullo stato dei vari componenti di Malware Protection Manager. | Funzione MpManagerStatusQueryEx (MpClient.h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Funzione MpManagerStatusQueryEx funzionalità dell'Windows legacy
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
ms.openlocfilehash: d8d7e3e6135a5f01691528480b760cfea422c78b9c032219f6e100da5ebd929d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961111"
---
# <a name="mpmanagerstatusqueryex-function"></a>Funzione MpManagerStatusQueryEx

Restituisce informazioni sullo stato dei vari componenti di Malware Protection Manager.

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

*hMpHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di Malware Protection Manager. Questo handle viene restituito dalla [**funzione MpManagerOpen.**](mpmanageropen.md)

</dd> <dt>

*dwFlag* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Controlla quali informazioni sulle query vengono restituite. Alcune informazioni sono costose e potrebbero non essere necessarie.



| Valore                                                                                                                                                                                                         | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**MP \_ STATUS \_ QUERY \_ FLAGS \_ NONE**</dt> </dl>       | Valore predefinito.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**MP \_ STATUS \_ QUERY \_ FLAG \_ NOSTATE**</dt> </dl> | Non eseguire query per ottenere informazioni sullo stato.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ Cambio\]
</dt> <dd>

Tipo: **PMPSTATUS \_ INFO**

Puntatore a una struttura che restituisce informazioni sullo stato relative alle ultime analisi, alle minacce attive e ai vari stati dei componenti. Vedere [**MPSTATUS \_ INFO**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**. Questa chiamata di funzione ha esito positivo anche se un servizio AntiMalware non è in esecuzione.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT non** riuscito. Il chiamante può usare la [**funzione MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**INFORMAZIONI \_ MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





