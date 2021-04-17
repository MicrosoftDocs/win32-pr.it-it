---
title: Metodo OnComplete INapServerCallback (NapSystemHealthValidator. h)
description: Usato da SHV per segnalare il completamento della richiesta asincrona.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Metodo OnComplete NAP
- Metodo OnComplete NAP, interfaccia INapServerCallback
- Interfaccia NAP di INapServerCallback, metodo OnComplete
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
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479343"
---
# <a name="inapservercallbackoncomplete-method"></a>Metodo INapServerCallback:: OnComplete

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapServerCallback:: OnComplete** viene usato da SHV per segnalare il completamento della richiesta asincrona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*richiesta* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) che rappresenta una richiesta di convalida.

</dd> <dt>

Codice errore  \[ in\]
</dt> <dd>

[**Codice di errore di protezione accesso alla rete**](nap-error-constants.md) che indica il motivo per cui non è stato possibile eseguire la convalida.

> [!Note]  
> In genere, il valore restituito del metodo [**INapSystemHealthValidationRequest:: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) viene passato a questo parametro. Tuttavia, se non è possibile chiamare **SetSoHResponse** a causa di un errore di rielaborazione, viene passato il valore restituito dal comando non riuscito.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

I validator devono restituire S \_ OK se la convalida [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) può essere completata, indipendentemente dal fatto che il **SoHRequest** abbia superato il controllo di integrità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





