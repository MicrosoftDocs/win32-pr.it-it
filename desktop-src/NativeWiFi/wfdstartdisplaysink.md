---
description: Esegue l'inizializzazione necessaria per consentire all'app chiamante di diventare un sink di visualizzazione Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Funzione WFDDisplaySinkStart (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528158"
---
# <a name="wfddisplaysinkstart-function"></a>WFDDisplaySinkStart (funzione)

Esegue l'inizializzazione necessaria per consentire all'app chiamante di diventare un sink di visualizzazione Miracast. L'app dovrebbe chiamarla una volta all'avvio.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uDeviceCategory* \[ in\]
</dt> <dd>

Categoria del dispositivo.

</dd> <dt>

*uSubCategory* \[ in\]
</dt> <dd>

Sottocategoria del dispositivo.

</dd> <dt>

*pCallbackContext* \[ in, facoltativo\]
</dt> <dd>

Puntatore di contesto facoltativo che viene passato alla funzione di callback specificata nel parametro *pfnCallback* .

</dd> <dt>

*pfnCallback* \[ in\]
</dt> <dd>

Puntatore alla funzione di callback da chiamare ogni volta che è presente una notifica per l'app. Le notifiche che è possibile inviare sono descritte [**in \_ \_ \_ \_ richiamata della notifica del sink di visualizzazione della direttiva**](wfd-display-sink-notification-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.



| Codice restituito                                                                                          | Descrizione                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ non \_ supportato**</dt> </dl> | Il sink di visualizzazione non è supportato in questo hardware.<br/> |



 

## <a name="remarks"></a>Commenti

Questa funzione esegue le attività seguenti:

-   Rende individuabile il PC
-   Imposta le informazioni sul dispositivo P2P in modo da riflettere la categoria e la sottocategoria specificata
-   Imposta la Miracast IEs su tutti i frame diretti di Wi-Fi con il tipo di dispositivo come sink
-   Registra il callback specificato da richiamare ogni volta che è presente una connessione in ingresso

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                      |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**richiamata della notifica del sink di \_ visualizzazione della direttiva. \_ \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




