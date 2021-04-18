---
description: Ottiene un handle per la finestra di dialogo in cui vengono visualizzati i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'Metodo IWiaAppErrorHandler:: GetWindow (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312423"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>Metodo IWiaAppErrorHandler:: GetWindow

Ottiene un handle per la finestra di dialogo in cui vengono visualizzati i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phwnd* \[ out\]
</dt> <dd>

Tipo: **HWND \** _

HWND utilizzato dal gestore degli errori dell'applicazione, dal gestore degli errori del driver e dal gestore degli errori predefinito per le finestre di dialogo del messaggio del dispositivo (sia errore che informativo). Il valore di output può essere _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

*phwnd* punta alla finestra passata in [**REPORTSTATUS**](-wia-iwiaerrorhandler-reportstatus.md) dal proxy WIA (Windows Image Acquisition) 2,0. Questa finestra deve rimanere valida per la durata del trasferimento dei dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




