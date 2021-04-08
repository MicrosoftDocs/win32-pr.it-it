---
title: Funzione MpManagerOpen (MpClient. h)
description: Stabilisce una connessione a malware Protection Manager nel computer locale.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerOpen
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
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743183"
---
# <a name="mpmanageropen-function"></a>MpManagerOpen (funzione)

Stabilisce una connessione a malware Protection Manager nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwReserved* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Riservato per utilizzi futuri. Deve essere 0.

</dd> <dt>

*phMpHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .

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

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





