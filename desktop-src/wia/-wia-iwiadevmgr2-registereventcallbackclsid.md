---
description: "Il metodo IWiaDevMgr2:: RegisterEventCallbackCLSID registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione."
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'Metodo IWiaDevMgr2:: RegisterEventCallbackCLSID (WIA. h)'
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
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527073"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>Metodo IWiaDevMgr2:: RegisterEventCallbackCLSID

Il metodo **IWiaDevMgr2:: RegisterEventCallbackCLSID** registra un'applicazione per ricevere eventi anche se l'applicazione non è in esecuzione.

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica i flag di registrazione. Può essere impostato sui valori seguenti:



| Flag di registrazione                | Significato                                           |
|----------------------------------|---------------------------------------------------|
| \_callback di \_ evento di registro WIA \_   | Eseguire la registrazione per l'evento.                           |
| \_callback di evento WIA Annulla registrazione \_ \_ | Eliminare la registrazione per l'evento.            |
| \_ \_ gestore predefinito set \_ WIA       | Impostare l'applicazione come gestore eventi predefinito. |



 

</dd> <dt>

*bstrDeviceID* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica un identificatore di dispositivo. Passare **null** per eseguire la registrazione per l'evento in tutti i dispositivi WIA 2,0.

</dd> <dt>

*pEventGUID* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Specifica l'evento per cui si sta registrando l'applicazione. Per un elenco degli eventi standard, vedere gli [identificatori di evento WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

_pClsID * \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Puntatore all'ID della classe dell'applicazione (_ * CLSID * *). Il sistema di runtime WIA 2,0 utilizza l'applicazione **CLSID** per avviare l'applicazione quando si verifica un evento per cui è registrata.

</dd> <dt>

*bstrName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'applicazione che registra per l'evento.

</dd> <dt>

*bstrDescription* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica una descrizione di testo dell'applicazione che esegue la registrazione per l'evento.

</dd> <dt>

*bstrIcon* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome di un file di immagine da utilizzare per l'icona dell'applicazione registrata per l'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Le applicazioni WIA 2,0 usano questo metodo per eseguire la registrazione in modo da ricevere gli eventi del dispositivo hardware. Dopo la chiamata di **IWiaDevMgr2:: RegisterEventCallbackCLSID** , l'applicazione viene registrata per la ricezione di eventi del dispositivo WIA 2,0 anche se non è in esecuzione.

Quando si verifica l'evento, il sistema WIA 2,0 determina quale applicazione è registrata per la ricezione dell'evento. Usa la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e il CLSID specificato nel parametro *pClsID* per creare un'istanza dell'applicazione, quindi chiama il metodo [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) per trasmettere le informazioni sull'evento all'applicazione.

Un'applicazione può richiamare il metodo [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) per enumerare le informazioni di registrazione degli eventi.

Se l'applicazione non è un componente Component Object Model registrato (COM) e non è compatibile con l'architettura WIA 2,0, usare il metodo [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) per registrare un'applicazione per gli eventi del dispositivo.

> [!Note]  
> In un'applicazione multithread non vi è alcuna garanzia che venga restituito il callback della notifica degli eventi sullo stesso thread che ha registrato il callback.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
