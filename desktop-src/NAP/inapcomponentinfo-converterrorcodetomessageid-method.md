---
title: Metodo INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: Viene utilizzato dal sistema NAP per richiedere che il client di integrità converta un codice di errore HRESULT in un ID messaggio.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- NAP metodo ConvertErrorCodeToMessageId
- Metodo ConvertErrorCodeToMessageId NAP, interfaccia INapComponentInfo
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
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478917"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>Metodo INapComponentInfo:: ConvertErrorCodeToMessageId

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo:: ConvertErrorCodeToMessageId** viene utilizzato dal sistema NAP per richiedere che il client di integrità converta un codice di errore HRESULT in un ID messaggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Codice errore  \[ in\]
</dt> <dd>

[**Codice di errore**](nap-error-constants.md) del sistema NAP che deve essere convertito in un **MessageID**.

</dd> <dt>

*msgid* \[ out\]
</dt> <dd>

Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa della stringa localizzata corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il **MessageID** restituito viene utilizzato dal sistema NAP per recuperare una stringa localizzata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





