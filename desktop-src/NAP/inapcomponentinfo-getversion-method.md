---
title: Metodo INapComponentInfo GetVersion (NapCommon.h)
description: Viene utilizzato dal sistema di Protezione accesso alla rete per ottenere la versione di un client di integrità.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- Metodo GetVersion NAP
- Metodo GetVersion NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo GetVersion
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e815c7d92ba9a33c07ba4d8d68c588ed0014019d0d173e0304c4a10204d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368383"
---
# <a name="inapcomponentinfogetversion-method"></a>Metodo INapComponentInfo::GetVersion

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo::GetVersion** viene usato dal sistema nap per ottenere la versione di un client di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*versione* \[ Cambio\]
</dt> <dd>

Puntatore a un [**MessageId**](nap-datatypes.md) che contiene l'ID risorsa della versione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





