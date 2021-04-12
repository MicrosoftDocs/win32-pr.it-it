---
title: Funzione MpHandleClose (MpClient. h)
description: Chiude l'handle restituito da MpManagerOpen, MpScanStart, MpThreatOpen o MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpHandleClose
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518754"
---
# <a name="mphandleclose-function"></a>MpHandleClose (funzione)

Chiude l'handle restituito da [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)o [**MpUpdateStart**](mpupdatestart.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle da chiudere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito. Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

La funzione può restituire l'errore specifico seguente:

| Codice restituito             | Descrizione                      |
|-------------------------|----------------------------------|
| E \_ vincere \_ un \_ handle non valido | L'handle specificato non è valido. |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> </dl>

 

 





