---
title: Funzione MpThreatEnumerate (MpClient. h)
description: Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione. Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpThreatEnumerate
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964587"
---
# <a name="mpthreatenumerate-function"></a>MpThreatEnumerate (funzione)

Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione. Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hThreatEnumHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per un contesto di enumerazione delle minacce restituito da [**MpThreatOpen**](mpthreatopen.md).

</dd> <dt>

*ppThreatInfo* \[ out\]
</dt> <dd>

Tipo: **PMPTHREAT \_ info \** _

Restituisce un puntatore a una struttura di informazioni sulle minacce, [_ *MPTHREAT \_ info* *](mpthreat-info.md). La struttura contiene informazioni quali ID minaccia, nome e gravità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se non sono presenti altri elementi da restituire, il valore restituito è **S \_ false**.

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

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**\_informazioni MPTHREAT**](mpthreat-info.md)
</dt> </dl>

 

 





