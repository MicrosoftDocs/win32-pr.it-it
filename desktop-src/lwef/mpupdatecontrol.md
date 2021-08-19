---
title: Funzione MpUpdateControl (MpClient.h)
description: Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Funzione MpUpdateControl funzionalità dell'Windows legacy
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69926f26b470ba41226883bdb32fab13c5d776858595c256fe70e7f95e898c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476273"
---
# <a name="mpupdatecontrol-function"></a>Funzione MpUpdateControl

Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite [**MpUpdateStart.**](mpupdatestart.md) La chiamata a questa funzione richiede privilegi di amministratore perché consente l'annullamento di un aggiornamento della firma a livello di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hUpdateHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per un'operazione di aggiornamento della firma asincrona. Questo handle viene restituito dalla [**funzione MpScanStart.**](mpscanstart.md)

</dd> <dt>

*UpdateControl* \[ Pollici\]
</dt> <dd>

Tipo: **MPCONTROL**

Specifica l'opzione del controllo di aggiornamento della firma. Deve essere il valore seguente:



| Valore                                                                                                                                                               | Significato                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl> | Interrompere l'operazione di aggiornamento della firma.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





