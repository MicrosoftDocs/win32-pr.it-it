---
title: Metodo INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Annulla la sottoscrizione da un server dei certificati di integrità (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- NAP metodo UnSubscribeCertByGroup
- Metodo UnSubscribeCertByGroup NAP, interfaccia INapCertRelyingParty
- Interfaccia INapCertRelyingParty NAP, metodo UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964362"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>Metodo INapCertRelyingParty:: UnSubscribeCertByGroup

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **UnSubscribeCertByGroup** Annulla la sottoscrizione da un server dei certificati di integrità (HCS).

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

 *ID* \[ in\]
</dt> <dd>

Oggetto [**EnforcementEntityId**](nap-datatypes.md) che contiene l'ID del client di imposizione che sta annullando la sottoscrizione.

</dd> <dt>

 *riservato* \[ in\]
</dt> <dd>

Deve essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Se non sono presenti altri Sottoscrittori di HCS, NapAgent eliminerà i certificati di integrità corrispondenti dall'archivio del computer locale.

Prima di chiamare questo metodo, chiamare [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).

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

 

 





