---
title: Funzione di callback PxeProviderInitialize
description: Un'esportazione da una libreria di collegamento dinamico (DLL) del provider che inizializza il provider e prepara la ricezione delle richieste client.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Funzione di callback PxeProviderInitialize servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302404"
---
# <a name="pxeproviderinitialize-callback-function"></a>Funzione di callback PxeProviderInitialize

Un'esportazione da una libreria di collegamento dinamico (DLL) del provider che inizializza il provider e prepara la ricezione delle richieste client. I provider sono necessari per esportare la funzione *PxeProviderInitialize* . Tutti i callback al provider devono essere registrati con una chiamata alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante l'elaborazione di *PxeProviderInitialize*. Alla restituzione di questa funzione, il provider deve essere completamente inizializzato e pronto per l'elaborazione delle richieste client.

## <a name="syntax"></a>Sintassi


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider. Questo handle deve essere archiviato dal provider e utilizzato nelle chiamate successive. Questo handle è valido fino a quando non viene chiamata la funzione di callback [*PxeProviderShutdown*](pxeprovidershutdown.md) .

</dd> <dt>

*hProviderKey* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema in cui devono essere archiviate le informazioni di configurazione del provider.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'inizializzazione del provider riesce, il callback dovrebbe restituire l' **errore \_ Success**. In caso di errore, dovrebbe essere restituito un codice di errore appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni server di servizi di distribuzione Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





