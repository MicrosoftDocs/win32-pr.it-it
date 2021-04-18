---
title: Funzione di callback PxeProviderShutdown
description: Chiamato per arrestare il provider.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Funzione di callback PxeProviderShutdown servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301602"
---
# <a name="pxeprovidershutdown-callback-function"></a>Funzione di callback PxeProviderShutdown

Chiamato per arrestare il provider. Questa funzione viene registrata chiamando la funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il parametro *CallbackType* impostato sull' **arresto del \_ callback \_ PXE**. Dopo la chiamata a questa funzione, l'handle *hProvider* passato alla funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) non è più valido.

## <a name="syntax"></a>Sintassi


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ in\]
</dt> <dd>

Valore di contesto passato alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'arresto del provider ha esito positivo, il callback dovrebbe restituire l' **errore \_ Success**. In caso di errore, dovrebbe essere restituito un codice di errore appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni server di servizi di distribuzione Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





