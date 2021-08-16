---
title: Funzione MpManagerOpen (MpClient.h)
description: Stabilisce una connessione a Malware Protection Manager nel computer locale.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Funzionalità dell'ambiente Windows mpManagerOpen
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324d013c46777ac48af32e6c91f557b7feda3a03fbdf0c21a7c79e8cf5e3d9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883366"
---
# <a name="mpmanageropen-function"></a>Funzione MpManagerOpen

Stabilisce una connessione a Malware Protection Manager nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwReserved* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Riservato per utilizzi futuri. Deve essere 0.

</dd> <dt>

*phMpHandle* \[ Cambio\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle per l'interfaccia di Malware Protection Manager. Questo handle deve essere chiuso con la [**funzione MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**. Questa chiamata di funzione avrà esito positivo anche se un servizio AntiMalware non è in esecuzione.

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

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





