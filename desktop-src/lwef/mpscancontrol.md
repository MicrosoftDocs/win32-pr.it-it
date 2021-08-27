---
title: Funzione MpScanControl (MpClient.h)
description: Consente il controllo di un'analisi avviata in modo asincrono tramite MpScanStart.
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
ms.openlocfilehash: 893fe1d01f9004c9dc2933a5bbb23c4b13fb8933a6121c41810c6e447e5eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114551"
---
# <a name="mpscancontrol-function"></a>Funzione MpScanControl

Consente il controllo di un'analisi avviata in modo asincrono tramite [**MpScanStart.**](mpscanstart.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hScanHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per un'operazione di analisi asincrona. Questo handle viene restituito dalla [**funzione MpScanStart.**](mpscanstart.md) Questo parametro può anche essere impostato sull'handle dell'interfaccia di Malware Protection Manager restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) per controllare un'analisi avviata dal sistema, nel qual caso il chiamante deve avere privilegi amministrativi.

</dd> <dt>

*ScanControl* \[ Pollici\]
</dt> <dd>

Tipo: **MPCONTROL**

Specifica un'opzione di controllo di analisi. Questo parametro deve essere una delle opzioni di controllo seguenti:



| Valore                                                                                                                                                                  | Significato                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**INTERRUZIONE DI \_ MPCONTROL**</dt> </dl>    | Interrompere l'operazione di analisi.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**MPCONTROL \_ PAUSE**</dt> </dl>    | Sospendere l'operazione di analisi.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**RIPRENDI \_ MPCONTROL**</dt> </dl> | Riprendere l'operazione di analisi sospesa.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





