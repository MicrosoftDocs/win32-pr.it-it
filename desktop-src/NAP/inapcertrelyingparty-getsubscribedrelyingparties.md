---
title: Metodo INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Ottiene un elenco di relying party che hanno sottoscritto.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- NAP metodo GetSubscribedRelyingParties
- Metodo GetSubscribedRelyingParties NAP, interfaccia INapCertRelyingParty
- Interfaccia INapCertRelyingParty NAP, metodo GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475490"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>Metodo INapCertRelyingParty:: GetSubscribedRelyingParties

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetSubscribedRelyingParties** ottiene un elenco di relying party che hanno sottoscritto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di out\]
</dt> <dd>

Puntatore a un [**EnforcementEntityCount**](nap-datatypes.md) contenente il numero di relying party sottoscritti.

</dd> <dt>

*relyingParties* \[ out\]
</dt> <dd>

Puntatore a un puntatore a un [**EnforcementEntityId**](nap-datatypes.md) che contiene l'elenco di relying party sottoscritti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il chiamante deve liberare il parametro *relyingParties* usando **CoTaskMemFree**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





