---
title: Metodo INapServerCallback OnComplete (NapSystemHealthValidator.h)
description: Usato dagli SHV per segnalare il completamento della richiesta asincrona.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Metodo OnComplete NAP
- Metodo OnComplete NAP , interfaccia INapServerCallback
- Interfaccia INapServerCallback NAP, metodo OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b0eb14663894eb1aac6911659eb452a1d50af59219b9c978215dc96de8a12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012589"
---
# <a name="inapservercallbackoncomplete-method"></a>Metodo INapServerCallback::OnComplete

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerCallback::OnComplete** viene usato dagli SHV per segnalare il completamento asincrono delle richieste.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*richiesta* \[ Pollici\]
</dt> <dd>

Puntatore a un [**oggetto INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) che rappresenta una richiesta di convalida.

</dd> <dt>

*errorCode* \[ Pollici\]
</dt> <dd>

Codice [**di errore di Protezione accesso**](nap-error-constants.md) alla rete che indica il motivo per cui non è stato possibile eseguire la convalida.

> [!Note]  
> In genere, il valore restituito del [**metodo INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) viene passato a questo parametro. Tuttavia, se non è stato possibile chiamare **SetSoHResponse** a causa di un errore di rielaborazione, viene passato il valore restituito dal comando non riuscito.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

I validator devono restituire S OK se la convalida SoHRequest può essere completata, indipendentemente dal fatto che \_ **SoHRequest** superi il controllo di integrità. [](/windows/win32/api/naptypes/ns-naptypes-soh)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





