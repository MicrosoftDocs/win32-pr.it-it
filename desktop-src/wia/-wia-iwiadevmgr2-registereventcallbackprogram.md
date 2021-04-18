---
description: "Il metodo IWiaDevMgr2:: RegisterEventCallbackProgram registra un'applicazione per la ricezione di eventi del dispositivo. Viene fornita principalmente per garantire la compatibilità con le applicazioni che non sono state scritte per Windows Image Acquisition (WIA) 2,0."
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'Metodo IWiaDevMgr2:: RegisterEventCallbackProgram (WIA. h)'
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
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308235"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>Metodo IWiaDevMgr2:: RegisterEventCallbackProgram

Il metodo **IWiaDevMgr2:: RegisterEventCallbackProgram** registra un'applicazione per la ricezione di eventi del dispositivo. Viene fornita principalmente per garantire la compatibilità con le applicazioni che non sono state scritte per Windows Image Acquisition (WIA) 2,0.

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Flag di registrazione. Può essere impostato sui valori seguenti.



| Valore                                                                                                                                                                                                           | Significato                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**\_callback di \_ evento di registro WIA \_**</dt> </dl>       | Eseguire la registrazione per l'evento.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**\_callback di evento WIA Annulla registrazione \_ \_**</dt> </dl> | Eliminare la registrazione per l'evento.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**\_ \_ gestore predefinito set \_ WIA**</dt> </dl>                   | Impostare l'applicazione come gestore eventi predefinito.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Identificatore del dispositivo. Passare **null** per eseguire la registrazione per l'evento in tutti i dispositivi WIA 2,0.

</dd> <dt>

*pEventGUID* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Evento per cui è registrata l'applicazione. Per un elenco di GUID evento validi, vedere gli [identificatori di evento WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

_bstrFullAppName * \[ in\]
</dt> <dd>

Tipo: **BSTR**

Nome completo del percorso dell'applicazione.

</dd> <dt>

*bstrCommandlineArg* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Argomenti della riga di comando appropriati per l'applicazione.

</dd> <dt>

*bstrName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Nome dell'applicazione. Il nome viene visualizzato all'utente quando più applicazioni si registrano per lo stesso evento.

</dd> <dt>

*bstrDescription* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Descrizione dell'applicazione. La descrizione viene visualizzata all'utente quando più applicazioni si registrano per lo stesso evento.

</dd> <dt>

*bstrIcon* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Icona che rappresenta l'applicazione. L'icona viene visualizzata all'utente quando più applicazioni si registrano per lo stesso evento. La stringa contiene il nome dell'applicazione e l'indice in base zero dell'icona separata da una virgola, ad esempio "MyApp,0". Potrebbe esserci più di un'icona che rappresenta un'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Usare **IWiaDevMgr2:: RegisterEventCallbackProgram** per registrare gli eventi relativi ai dispositivi hardware. Quando si verifica un evento per cui è registrata un'applicazione, viene avviata l'applicazione e le informazioni sull'evento vengono trasmesse all'applicazione.

Usare il metodo [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) per recuperare un puntatore a un oggetto enumeratore per le proprietà di registrazione eventi.

Usare il metodo **IWiaDevMgr2:: RegisterEventCallbackProgram** per la compatibilità con le versioni precedenti con le applicazioni non scritte per l'architettura WIA 2,0. Usare le interfacce Component Object Model (COM) fornite dall'architettura WIA 2,0 per le nuove applicazioni. In particolare, chiamare [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) per registrare una nuova applicazione per gli eventi del dispositivo.

In genere, questo metodo viene chiamato da un programma di installazione o da uno script. Il programma o lo script di installazione registra l'applicazione per la ricezione di eventi del dispositivo WIA 2,0. Quando si verifica l'evento, l'applicazione viene avviata dal sistema di runtime WIA 2,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




