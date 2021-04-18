---
title: Funzione di callback PxeProviderServiceControl
description: Chiamato quando il servizio WDS riceve un codice di controllo del servizio.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Funzione di callback PxeProviderServiceControl servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301603"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>Funzione di callback PxeProviderServiceControl

Chiamato quando il servizio WDS riceve un codice di controllo del servizio. Questa funzione di callback viene registrata chiamando la funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il parametro *CallbackType* impostato sul **\_ \_ \_ controllo del servizio di callback PXE**.

## <a name="syntax"></a>Sintassi


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ in\]
</dt> <dd>

Valore di contesto passato alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> <dt>

*dwControl* 
</dt> <dd>

Codice di controllo. Per l'elenco dei valori possibili, vedere il parametro *dwControl* della funzione [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .

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

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

