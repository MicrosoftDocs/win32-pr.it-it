---
title: Metodo INapComponentInfo GetFriendlyName (NapCommon.h)
description: Viene utilizzato dal sistema di Protezione accesso alla rete per ottenere il nome descrittivo di un client di integrità.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Metodo GetFriendlyName NAP
- Metodo GetFriendlyName NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo GetFriendlyName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3236a9d4959c441816aa476993d95286b4ac1f710ccdb63325aba225bfabb106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799716"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a>Metodo INapComponentInfo::GetFriendlyName

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo::GetFriendlyName** viene usato dal sistema nap per ottenere il nome descrittivo di un client di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*friendlyName* \[ Cambio\]
</dt> <dd>

Puntatore a un [**MessageId**](nap-datatypes.md) che contiene l'ID risorsa del nome descrittivo.

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

 

 





