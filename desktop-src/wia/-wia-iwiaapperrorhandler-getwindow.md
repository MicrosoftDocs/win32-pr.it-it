---
description: Ottiene un handle per la finestra di dialogo che visualizza i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: Metodo IWiaAppErrorHandler::GetWindow (Wia.h)
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
ms.openlocfilehash: 1bac7ba2f2f9d394218d851f9bbe7939168c2abbc7df5fb8c57a52f29fa6e2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965760"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>Metodo IWiaAppErrorHandler::GetWindow

Ottiene un handle per la finestra di dialogo che visualizza i messaggi di errore e fornisce uno o più pulsanti per continuare, annullare o interrompere l'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phwnd* \[ Cambio\]
</dt> <dd>

Tipo: **HWND \***

HWND usato dal gestore degli errori dell'applicazione, dal gestore degli errori del driver e dal gestore degli errori predefinito per le finestre di dialogo dei messaggi del dispositivo (errore e informativo). Il valore di output può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

*phwnd* punta alla finestra passata a [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) dal proxy Windows Image Acquisition (WIA) 2.0. Questa finestra deve rimanere valida per la durata del trasferimento dei dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




