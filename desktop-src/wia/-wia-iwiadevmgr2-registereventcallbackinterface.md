---
description: Registra un'applicazione in esecuzione per Windows di eventi di acquisizione di immagini (WIA) 2.0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: Metodo IWiaDevMgr2::RegisterEventCallbackInterface (Wia.h)
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
ms.openlocfilehash: e2658654254257c707d12f4e676aee3371f0ad491dfedeb0637508ca3f33a057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965641"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>Metodo IWiaDevMgr2::RegisterEventCallbackInterface

Registra un'applicazione in esecuzione per Windows di eventi di acquisizione di immagini (WIA) 2.0.

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

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'identificatore univoco di un dispositivo WIA 2.0. Impostare questo parametro su **NULL per** registrarsi per l'evento in tutti i dispositivi WIA 2.0.

</dd> <dt>

*pEventGUID* \[ Pollici\]
</dt> <dd>

Tipo: **CONST \* GUID**

Specifica un puntatore all'identificatore evento per cui l'applicazione sta registrando. Per gli identificatori di evento standard, vedere Identificatori di evento [WIA.](-wia-wia-event-identifiers.md)

</dd> <dt>

*pIWiaEventCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Specifica un puntatore [**all'interfaccia IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) utilizzata da WIA 2.0 per inviare la notifica degli eventi.

</dd> <dt>

*pEventObject* \[ Cambio\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Riceve l'indirizzo di un puntatore [all'interfaccia IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce i codici di errore COM standard o gli elementi seguenti.



| Codice restituito                                                                               | Descrizione                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Impossibile [restituire l'interfaccia IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown) <br/> |



 

## <a name="remarks"></a>Commenti

> [!WARNING]
> L'uso dei metodi [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface** e [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) dello stesso processo dopo il riavvio del servizio still image può causare una violazione di accesso, se le funzioni sono state usate prima dell'arresto del servizio.

 

Quando le applicazioni WIA 2.0 iniziano l'esecuzione, usano questo metodo per registrarsi per ricevere eventi del dispositivo hardware. Ciò impedisce il riavvio dell'applicazione quando si verifica un altro evento per cui è registrata. Quando un'applicazione chiama **IWiaDevMgr2::RegisterEventCallbackInterface** per registrarsi per ricevere eventi WIA 2.0 da un dispositivo, gli eventi registrati vengono indirizzati al programma da WIA 2.0.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro pEventObject.*

> [!Note]  
> In un'applicazione multithreading, il callback di notifica degli eventi può essere eseguito in un thread diverso da quello che ha registrato il callback.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
