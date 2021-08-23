---
title: Metodo INapServerInfo GetFailureCategoryMappings (NapServerManagement.h)
description: Recupera i mapping della categoria di errore per un oggetto SHA o SHV specificato.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Metodo GetFailureCategoryMappings nap
- Metodo GetFailureCategoryMappings NAP , interfaccia INapServerInfo
- Interfaccia INapServerInfo NAP, metodo GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13fcd87105eace269d3b8f395392c8a0ba275a135c212863ef69e45e597eb752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144384"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a>Metodo INapServerInfo::GetFailureCategoryMappings

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerInfo::GetFailureCategoryMappings** recupera i mapping della categoria di errore per un oggetto SHA o SHV specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* \[ in\]
</dt> <dd>

[**SystemHealthEntityId**](nap-type-constants.md) che contiene l'identificatore univoco dell'SHA o della SHV.

</dd> <dt>

*mapping* \[ Cambio\]
</dt> <dd>

Puntatore a un [**oggetto FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) che contiene i dati di mapping.

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

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





