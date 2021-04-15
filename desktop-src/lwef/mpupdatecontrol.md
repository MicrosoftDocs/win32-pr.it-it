---
title: Funzione MpUpdateControl (MpClient. h)
description: Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpUpdateControl
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
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477656"
---
# <a name="mpupdatecontrol-function"></a>MpUpdateControl (funzione)

Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite [**MpUpdateStart**](mpupdatestart.md). La chiamata a questa funzione richiede privilegi amministrativi perché consente l'annullamento di un aggiornamento della firma a livello di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hUpdateHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per un'operazione di aggiornamento della firma asincrona. Questo handle viene restituito dalla funzione [**MpScanStart**](mpscanstart.md) .

</dd> <dt>

*UpdateControl* \[ in\]
</dt> <dd>

Tipo: **MPCONTROL**

Specifica l'opzione di controllo dell'aggiornamento della firma. Deve essere il valore seguente:



| Valore                                                                                                                                                               | Significato                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**\_interruzione MPCONTROL**</dt> </dl> | Interrompere l'operazione di aggiornamento della firma.<br/> |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





