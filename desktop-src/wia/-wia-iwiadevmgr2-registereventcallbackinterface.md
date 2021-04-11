---
description: Registra un'applicazione in esecuzione per la notifica degli eventi di Windows Image Acquisition (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'Metodo IWiaDevMgr2:: RegisterEventCallbackInterface (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231553"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>Metodo IWiaDevMgr2:: RegisterEventCallbackInterface

Registra un'applicazione in esecuzione per la notifica degli eventi di Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'identificatore univoco di un dispositivo WIA 2,0. Impostare questo parametro su **null** per registrarsi per l'evento in tutti i dispositivi WIA 2,0.

</dd> <dt>

*pEventGUID* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Specifica un puntatore all'identificatore dell'evento per cui è registrata l'applicazione. Vedere gli [identificatori di evento WIA](-wia-wia-event-identifiers.md) per gli identificatori di evento standard.

</dd> <dt>

_pIWiaEventCallback * \[ in\]
</dt> <dd>

Tipo: **[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _

Specifica un puntatore all'interfaccia [_ *IWiaEventCallback* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) utilizzata da WIA 2,0 per inviare la notifica degli eventi.

</dd> <dt>

*pEventObject* \[ out\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce i codici di errore COM standard o gli elementi seguenti.



| Codice restituito                                                                               | Descrizione                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Non è possibile restituire l'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . <br/> |



 

## <a name="remarks"></a>Commenti

> [!WARNING]
> L'uso dei metodi [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: RegisterEventCallbackInterface** e [**devicemanager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) dello stesso processo dopo il riavvio del servizio Still Image può causare una violazione di accesso, se le funzioni sono state usate prima dell'arresto del servizio.

 

Quando le applicazioni WIA 2,0 iniziano l'esecuzione, usano questo metodo per eseguire la registrazione in modo da ricevere gli eventi del dispositivo hardware. In questo modo si impedisce che l'applicazione venga riavviata quando si verifica un altro evento per cui è registrata. Quando un'applicazione chiama **IWiaDevMgr2:: RegisterEventCallbackInterface** per registrarsi per ricevere eventi WIA 2,0 da un dispositivo, gli eventi registrati vengono indirizzati al programma da WIA 2,0.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *pEventObject* .

> [!Note]  
> In un'applicazione multithread, il callback della notifica degli eventi può essere presente in un thread diverso da quello che ha registrato il callback.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
