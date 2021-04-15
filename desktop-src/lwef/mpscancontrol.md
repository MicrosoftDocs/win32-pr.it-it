---
title: Funzione MpScanControl (MpClient. h)
description: Consente il controllo di un'analisi che è stata avviata in modo asincrono tramite MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476498"
---
# <a name="mpscancontrol-function"></a>MpScanControl (funzione)

Consente il controllo di un'analisi che è stata avviata in modo asincrono tramite [**MpScanStart**](mpscanstart.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hScanHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per un'operazione di analisi asincrona. Questo handle viene restituito dalla funzione [**MpScanStart**](mpscanstart.md) . Questo parametro può essere impostato anche sull'handle di interfaccia di malware Protection Manager restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) per controllare un'analisi avviata dal sistema, nel qual caso il chiamante deve avere privilegi amministrativi.

</dd> <dt>

*ScanControl* \[ in\]
</dt> <dd>

Tipo: **MPCONTROL**

Specifica un'opzione di controllo Scan. Questo parametro deve essere una delle opzioni di controllo seguenti:



| Valore                                                                                                                                                                  | Significato                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_interruzione MPCONTROL**</dt> </dl>    | Interrompere l'operazione di analisi.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**MPCONTROL \_ pausa**</dt> </dl>    | Sospendere l'operazione di analisi.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**Riprendi MPCONTROL \_**</dt> </dl> | Riprendere l'operazione di analisi sospesa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





