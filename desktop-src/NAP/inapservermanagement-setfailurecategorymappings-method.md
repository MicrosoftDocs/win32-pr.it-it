---
title: Metodo INapServerManagement SetFailureCategoryMappings (NapServerManagement.h)
description: Viene usato per impostare i mapping della categoria di errore della SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Metodo SetFailureCategoryMappings nap
- Metodo SetFailureCategoryMappings NAP , interfaccia INapServerManagement
- Metodo SetFailureCategoryMappings dell'interfaccia INapServerManagement nap
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22bc51edf887d26bf34f59932248c62bfca86199771a2b971a10e9c1b323eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939615"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>Metodo INapServerManagement::SetFailureCategoryMappings

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerManagement::SetFailureCategoryMappings** viene usato per impostare i mapping della categoria di errore shv.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* \[ in\]
</dt> <dd>

[**SystemHealthEntityId**](nap-type-constants.md) che contiene l'identificatore univoco della shv.

</dd> <dt>

*mapping* \[ Pollici\]
</dt> <dd>

Struttura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) che contiene i dati di mapping della categoria di errori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





