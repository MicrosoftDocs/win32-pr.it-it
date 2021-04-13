---
title: Funzione di callback PxeProviderRecvRequest
description: Chiamato quando viene ricevuta una richiesta da un client.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Funzione di callback PxeProviderRecvRequest servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400627"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>Funzione di callback PxeProviderRecvRequest

Chiamato quando viene ricevuta una richiesta da un client. Questa funzione viene registrata chiamando la funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il parametro *CallbackType* impostato su **Request PXE \_ callback \_ ricezione \_**.

## <a name="syntax"></a>Sintassi


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hClientRequest* \[ in\]
</dt> <dd>

Handle per una richiesta ricevuta da un client.

</dd> <dt>

*pPacket* \[ in\]
</dt> <dd>

Puntatore al buffer di memoria che contiene il pacchetto ricevuto.

</dd> <dt>

*uPacketLen* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer a cui punta il parametro *pPacket* .

</dd> <dt>

*pLocalAddress* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ indirizzi PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) che contiene l'indirizzo locale in cui è stato ricevuto il pacchetto.

</dd> <dt>

*pRemoteAddress* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ indirizzi PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) che contiene l'indirizzo di origine del pacchetto.

</dd> <dt>

*patto* \[ out\]
</dt> <dd>

Specifica l'azione che deve essere eseguita dal sistema.



| Valore                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <dt>**PXE \_ BA \_ avvio**</dt> <dt>1</dt> </dl>                | Il provider ha risposto a un client con un pacchetto di risposta DHCP standard che contiene un percorso del programma di avvio di rete. La restituzione di questa azione significa che il provider ha completato correttamente la richiesta del client chiamando la funzione [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) almeno una volta.<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <dt>**PXE \_ BA \_ personalizzata**</dt> <dt>2</dt> </dl>       | Il provider ha risposto a un client usando una risposta personalizzata che non è conforme alle specifiche DHCP. La restituzione di questa azione significa che il provider ha completato correttamente la richiesta del client chiamando la funzione [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) almeno una volta.<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <dt>**PXE \_ BA \_ ignorare**</dt> <dt>3</dt> </dl>       | Il provider non desidera servire la richiesta client e la richiesta non deve essere passata al provider successivo. Tutte le risorse associate alla richiesta client vengono rilasciate e la richiesta del client viene ignorata. I provider possono anche usare questo valore se riconoscono il client ma la richiesta non è valida.<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <dt>**PXE \_ BA \_ rifiutato**</dt> <dt>4</dt> </dl> | Il provider non desidera servire la richiesta client. Il sistema passa la richiesta al provider successivo nell'elenco dei provider registrati. Se questo è l'ultimo provider nell'elenco, vengono rilasciate tutte le risorse associate alla richiesta client e la richiesta del client viene ignorata.<br/>                     |



 

</dd> <dt>

*pContext* \[ in\]
</dt> <dd>

Valore di contesto passato alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il provider ha elaborato correttamente la richiesta del client, il callback deve restituire un **errore di \_ esito positivo** e l' **\_ \_ azione di avvio PXE** a cui punta il parametro di *patto* contiene l'azione di avvio appropriata per la richiesta. Se il provider elaborerà la richiesta client in modo asincrono, il callback deve restituire l' **errore \_ io \_ in sospeso** e chiamare la funzione [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) quando la richiesta client è stata elaborata. In caso di errore, dovrebbe essere restituito un codice di errore appropriato e il sistema continuerà come se fosse stata specificata l'azione di avvio **\_ \_ rifiutato da PXE BA** .

## <a name="remarks"></a>Commenti

Il tipo di pacchetti visualizzati da un provider può essere modificato con la funzione [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni server di servizi di distribuzione Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





