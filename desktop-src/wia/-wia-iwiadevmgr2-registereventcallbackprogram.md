---
description: Il metodo IWiaDevMgr2::RegisterEventCallbackProgram registra un'applicazione per ricevere gli eventi del dispositivo. Viene fornito principalmente per la compatibilità con le versioni precedenti con le applicazioni che non sono state scritte per Windows'acquisizione di immagini (WIA) 2.0.
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: Metodo IWiaDevMgr2::RegisterEventCallbackProgram (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ebc99e61bf038c8db2ea537a1f8a5933ad512d21ec05cf51f6f8b7af5ede2b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441299"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>Metodo IWiaDevMgr2::RegisterEventCallbackProgram

Il **metodo IWiaDevMgr2::RegisterEventCallbackProgram** registra un'applicazione per ricevere gli eventi del dispositivo. Viene fornito principalmente per la compatibilità con le versioni precedenti con le applicazioni che non sono state scritte per Windows'acquisizione di immagini (WIA) 2.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Flag di registrazione. Può essere impostato su i valori seguenti.



| Valore                                                                                                                                                                                                           | Significato                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**CALLBACK \_ DELL'EVENTO DI \_ REGISTRAZIONE WIA \_**</dt> </dl>       | Registrarsi per l'evento.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**CALLBACK \_ DELL'EVENTO WIA UNREGISTER \_ \_**</dt> </dl> | Eliminare la registrazione per l'evento.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**WIA \_ SET \_ DEFAULT \_ HANDLER**</dt> </dl>                   | Impostare l'applicazione come gestore eventi predefinito.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Identificatore del dispositivo. Passare **NULL per** registrarsi per l'evento in tutti i dispositivi WIA 2.0.

</dd> <dt>

*pEventGUID* \[ Pollici\]
</dt> <dd>

Tipo: **CONST \* GUID**

Evento per cui l'applicazione sta registrando. Per un elenco di GUID di evento validi, vedere [IDENTIFICATORI DI EVENTI WIA.](-wia-wia-event-identifiers.md)

</dd> <dt>

*bstrFullAppName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Nome completo del percorso dell'applicazione.

</dd> <dt>

*bstrCommandlineArg* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Argomenti della riga di comando appropriati per l'applicazione.

</dd> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Nome dell'applicazione. Il nome viene visualizzato all'utente quando più applicazioni si registrano per lo stesso evento.

</dd> <dt>

*bstrDescription* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Descrizione dell'applicazione. La descrizione viene visualizzata all'utente quando più applicazioni si registrano per lo stesso evento.

</dd> <dt>

*bstrIcon* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Icona che rappresenta l'applicazione. L'icona viene visualizzata all'utente quando più applicazioni si registrano per lo stesso evento. La stringa contiene il nome dell'applicazione e l'indice in base zero dell'icona separati da una virgola, ad esempio "MyApp, 0". Potrebbero essere presenti più icone che rappresentano un'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare **IWiaDevMgr2::RegisterEventCallbackProgram** per eseguire la registrazione per gli eventi del dispositivo hardware. Quando si verifica un evento per cui è registrata un'applicazione, l'applicazione viene avviata e le informazioni sull'evento vengono trasmesse all'applicazione.

Usare il [**metodo EnumRegisterEventInfo per**](-wia-iwiaitem2-enumregistereventinfo.md) recuperare un puntatore a un oggetto enumeratore per le proprietà di registrazione degli eventi.

Usare solo il **metodo IWiaDevMgr2::RegisterEventCallbackProgram** per la compatibilità con le versioni precedenti con le applicazioni non scritte per l'architettura WIA 2.0. Usare le interfacce Component Object Model (COM) fornite dall'architettura WIA 2.0 per le nuove applicazioni. In particolare, chiamare [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) o [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) per registrare una nuova applicazione per gli eventi del dispositivo.

In genere, questo metodo viene chiamato da un programma di installazione o da uno script. Il programma di installazione o lo script registra l'applicazione per ricevere gli eventi del dispositivo WIA 2.0. Quando si verifica l'evento, l'applicazione viene avviata dal sistema di run-time WIA 2.0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 




