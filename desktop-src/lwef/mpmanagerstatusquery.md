---
title: Funzione MpManagerStatusQuery (MpClient.h)
description: Restituisce informazioni sullo stato dei vari componenti di Malware Protection Manager. | Funzione MpManagerStatusQuery (MpClient.h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Funzione MpManagerStatusQuery legacy Windows'ambiente
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d05751f30e1579ef8b12e31a4f858469b1c997cf9c29d7643c0600a133840fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883376"
---
# <a name="mpmanagerstatusquery-function"></a>Funzione MpManagerStatusQuery

\[**MpManagerStatusQuery** non è supportato e potrebbe essere modificato o non disponibile in futuro. Usare invece [**MpManagerStatusQueryEx.**](mpmanagerstatusqueryex.md)\]

Restituisce informazioni sullo stato dei vari componenti di Malware Protection Manager.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
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

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**INFORMAZIONI \_ MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





