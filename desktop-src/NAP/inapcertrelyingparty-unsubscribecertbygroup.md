---
title: Metodo INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty.h)
description: Annulla la sottoscrizione a un server di certificati di integrità (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Metodo UnSubscribeCertByGroup NAP
- Metodo UnSubscribeCertByGroup NAP , interfaccia INapCertRelyingParty
- Metodo UnSubscribeCertByGroup dell'interfaccia INapCertRelyingParty NAP
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
ms.openlocfilehash: 7d8b9f5398ba63c0e6108adfefd51d0546180db4536dbd95615e5b15dddde523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940219"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>Metodo INapCertRelyingParty::UnSubscribeCertByGroup

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo UnSubscribeCertByGroup** annulla la sottoscrizione a un server certificati di integrità (HCS).

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

 *id* \[ in\]
</dt> <dd>

[**EnforcementEntityId che**](nap-datatypes.md) contiene l'ID del client di imposizione che sta annullando la sottoscrizione.

</dd> <dt>

 *riservato* \[ Pollici\]
</dt> <dd>

Deve essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Se non sono presenti altri sottoscrittori del servizio HCS, NapAgent eliminerà i certificati di integrità corrispondenti dall'archivio del computer locale.

Prima di chiamare questo metodo, [**chiamare SubscribeCertByGroup.**](inapcertrelyingparty-subscribecertbygroup.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapCertRelyingParty.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





