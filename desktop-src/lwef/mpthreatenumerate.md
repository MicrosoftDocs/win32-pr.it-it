---
title: Funzione MpThreatEnumerate (MpClient.h)
description: Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione. Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Funzione MpThreatEnumerate legacy Windows dell'ambiente
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
ms.openlocfilehash: 9525ad44901bd62044721e634559e1c803b88b05e9250097d939b3a5a04d229a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943831"
---
# <a name="mpthreatenumerate-function"></a>Funzione MpThreatEnumerate

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

*hThreatEnumHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle a un contesto di enumerazione delle minacce restituito [**da MpThreatOpen.**](mpthreatopen.md)

</dd> <dt>

*ppThreatInfo* \[ Cambio\]
</dt> <dd>

Tipo: **PMPTHREAT \_ \* INFO**

Restituisce un puntatore a una struttura di informazioni sulle minacce, [**MPTHREAT \_ INFO.**](mpthreat-info.md) La struttura contiene informazioni quali ID minaccia, nome e gravità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se non sono presenti altri elementi per restituire il valore restituito, il valore restituito è **S \_ FALSE.**

Se la funzione ha esito negativo, il valore restituito è un **codice HRESULT non** riuscito. Il chiamante può usare la [**funzione MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

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

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**INFORMAZIONI SU \_ MPTHREAT**](mpthreat-info.md)
</dt> </dl>

 

 





