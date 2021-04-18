---
title: Metodo INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: Sottoscrive un server di certificazione integrità (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- NAP metodo SubscribeCertByGroup
- Metodo SubscribeCertByGroup NAP, interfaccia INapCertRelyingParty
- Interfaccia INapCertRelyingParty NAP, metodo SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301814"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>Metodo INapCertRelyingParty:: SubscribeCertByGroup

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **SubscribeCertByGroup** sottoscrive un server dei certificati di integrità (HCS). HCS deve essere già registrato prima della sottoscrizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

 *ID* \[ in\]
</dt> <dd>

Oggetto [**EnforcementEntityId**](nap-datatypes.md) che contiene l'ID del client di imposizione che sta sottoscrivendo.

</dd> <dt>

*subscriberName* \[ in\]
</dt> <dd>

Nome del Sottoscrittore.

> [!Note]  
> Attualmente viene usato solo a scopo di registrazione.

 

</dd> <dt>

*riservato* \[ in\]
</dt> <dd>

Deve essere **null**.

</dd> <dt>

*certExists* \[ out\]
</dt> <dd>

Indica se un certificato di integrità di questo HCS è già gestito da NapAgent ed è presente nell'archivio del computer. Se **true**, un certificato di integrità è già in fase di manutenzione ed è presente. Se **false**, un certificato di integrità non viene attualmente mantenuto e presente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

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

 

 





