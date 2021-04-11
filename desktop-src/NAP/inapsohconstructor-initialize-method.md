---
title: Metodo Initialize INapSoHConstructor (NapProtocol. h)
description: Inizializza un pacchetto di protocollo di rapporto di integrità nel sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapSoHConstructor
- Interfaccia NAP di INapSoHConstructor, metodo Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964147"
---
# <a name="inapsohconstructorinitialize-method"></a>Metodo INapSoHConstructor:: Initialize

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHConstructor:: Initialize** Inizializza un pacchetto di protocollo di rapporto di integrità nel sistema NAP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'SHA o del servizio di convalida dell'integrità di sistema che costruisce il pacchetto.

</dd> <dt>

*richiesta* \[ in\]
</dt> <dd>

**Bool** che è **true** se il pacchetto deve essere un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se è un **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato una sola volta per ogni pacchetto.

Il [SystemHealthEntityId](nap-datatypes.md) specificato in *ID* è il primo TLV nel pacchetto SOH appena costruito e ha il tipo di attributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





