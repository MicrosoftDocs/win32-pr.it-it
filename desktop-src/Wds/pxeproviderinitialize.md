---
title: Funzione di callback PxeProviderInitialize
description: Esportazione da una libreria a collegamento dinamico (DLL) del provider che inizializza il provider e lo prepara per ricevere le richieste del client.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Funzione di callback PxeProviderInitialize Windows Deployment Services
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb7ba32049dc3ef70085a489b499d90b92ec6155323b650df0e2b2f839bbdf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098661"
---
# <a name="pxeproviderinitialize-callback-function"></a>Funzione di callback PxeProviderInitialize

Esportazione da una libreria a collegamento dinamico (DLL) del provider che inizializza il provider e lo prepara per ricevere le richieste del client. I provider sono necessari per esportare *la funzione PxeProviderInitialize.* Tutti i callback al provider devono essere registrati con una chiamata alla [**funzione PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante l'elaborazione *di PxeProviderInitialize.* Al ritorno di questa funzione, il provider deve essere completamente inizializzato e pronto per elaborare le richieste client.

## <a name="syntax"></a>Sintassi


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* \[ Pollici\]
</dt> <dd>

Handle per l'istanza del provider. Questo handle deve essere archiviato dal provider e usato in qualsiasi chiamata successiva. Questo handle è valido fino a quando non viene chiamata la funzione di callback [*PxeProviderShutdown.*](pxeprovidershutdown.md)

</dd> <dt>

*hProviderKey* \[ Pollici\]
</dt> <dd>

Handle a una chiave del Registro di sistema in cui devono essere archiviate le informazioni di configurazione del provider.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'inizializzazione del provider ha esito positivo, il callback deve restituire **ERROR \_ SUCCESS**. In caso di errore, deve essere restituito un codice di errore appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2003 con solo app desktop SP2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Funzioni del server di Servizi di distribuzione](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





