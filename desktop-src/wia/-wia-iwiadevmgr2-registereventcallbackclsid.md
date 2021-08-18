---
description: Il metodo IWiaDevMgr2::RegisterEventCallbackCLSID registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione.
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: Metodo IWiaDevMgr2::RegisterEventCallbackCLSID (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9137fdd33f59eb841a54e84a6d12bb0b08968ac29c8737afbf56f66c57176c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965649"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>Metodo IWiaDevMgr2::RegisterEventCallbackCLSID

Il **metodo IWiaDevMgr2::RegisterEventCallbackCLSID** registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica i flag di registrazione. Può essere impostato su i valori seguenti:



| Flag di registrazione                | Significato                                           |
|----------------------------------|---------------------------------------------------|
| CALLBACK \_ DELL'EVENTO DI \_ REGISTRAZIONE WIA \_   | Registrarsi per l'evento.                           |
| CALLBACK \_ DELL'EVENTO WIA UNREGISTER \_ \_ | Eliminare la registrazione per l'evento.            |
| WIA \_ SET \_ DEFAULT \_ HANDLER       | Impostare l'applicazione come gestore eventi predefinito. |



 

</dd> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica un identificatore di dispositivo. Passare **NULL per** registrarsi per l'evento in tutti i dispositivi WIA 2.0.

</dd> <dt>

*pEventGUID* \[ Pollici\]
</dt> <dd>

Tipo: **CONST \* GUID**

Specifica l'evento per cui l'applicazione sta registrando. Per un elenco di eventi standard, vedere [IDENTIFICATORI DI EVENTI WIA.](-wia-wia-event-identifiers.md)

</dd> <dt>

*pClsID* \[ Pollici\]
</dt> <dd>

Tipo: **CONST \* GUID**

Puntatore all'ID di classe **dell'applicazione ( CLSID**). Il sistema di run-time WIA 2.0 usa il **CLSID** dell'applicazione per avviare l'applicazione quando si verifica un evento per cui è registrato.

</dd> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'applicazione che si registra per l'evento.

</dd> <dt>

*bstrDescription* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica una descrizione testuale dell'applicazione che si registra per l'evento.

</dd> <dt>

*bstrIcon* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome di un file di immagine da utilizzare per l'icona per l'applicazione che si registra per l'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Le applicazioni WIA 2.0 usano questo metodo per eseguire la registrazione per ricevere eventi del dispositivo hardware. Dopo **la chiamata a IWiaDevMgr2::RegisterEventCallbackCLSID,** l'applicazione viene registrata per ricevere gli eventi del dispositivo WIA 2.0 anche se non è in esecuzione.

Quando si verifica l'evento, il sistema WIA 2.0 determina quale applicazione è registrata per ricevere l'evento. Usa la [funzione CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e il CLSID specificato nel *parametro pClsID* per creare un'istanza dell'applicazione e quindi chiama il [**metodo ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) per trasmettere le informazioni sull'evento all'applicazione.

Un'applicazione può richiamare il [**metodo EnumRegisterEventInfo per**](-wia-iwiaitem2-enumregistereventinfo.md) enumerare le informazioni di registrazione dell'evento.

Se l'applicazione non è un componente Component Object Model (COM) registrato e non è compatibile con l'architettura WIA 2.0, usare il metodo [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) per registrare un'applicazione per gli eventi del dispositivo.

> [!Note]  
> In un'applicazione multi-thread non è garantito che il callback di notifica degli eventi sia restituito nello stesso thread che ha registrato il callback.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 
