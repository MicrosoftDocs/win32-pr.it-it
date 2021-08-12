---
title: Metodo INapComponentInfo ConvertErrorCodeToMessageId (NapCommon.h)
description: Viene usato dal sistema di Protezione accesso alla rete per richiedere al client di integrità di convertire un codice di errore HRESULT in un ID messaggio.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Metodo ConvertErrorCodeToMessageId nap
- Metodo ConvertErrorCodeToMessageId NAP , interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c670585674713d114f6505a0c3211d599663545f6b06a40669f7fba8b7eddf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621730"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>Metodo INapComponentInfo::ConvertErrorCodeToMessageId

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo::ConvertErrorCodeToMessageId** viene usato dal sistema di Protezione accesso alla rete per richiedere al client di integrità di convertire un codice di errore HRESULT in un ID messaggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*errorCode* \[ Pollici\]
</dt> <dd>

Codice [**di errore**](nap-error-constants.md) del sistema di Protezione accesso alla rete da convertire in **MessageId.**

</dd> <dt>

*msgId* \[ Cambio\]
</dt> <dd>

Puntatore a un [**MessageId**](nap-datatypes.md) che contiene l'ID risorsa della stringa localizzata corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il **MessageId restituito** viene usato dal sistema di Protezione accesso alla rete per recuperare una stringa localizzata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





