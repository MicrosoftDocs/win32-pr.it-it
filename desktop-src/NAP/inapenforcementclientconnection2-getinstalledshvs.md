---
title: Metodo GetInstalledShvs INapEnforcementClientConnection2 (NapEnforcementClient.h)
description: Usato dall'agente protezione accesso alla rete per eseguire query sui validator dell'integrità del sistema installati nel client.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Metodo GetInstalledShvs nap
- Metodo GetInstalledShvs NAP , interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 NAP, metodo GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40cb18f749adc9a1b7003a777cc821fb5e003b83322a7d54c2efda4b8e5739f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939642"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>Metodo INapEnforcementClientConnection2::GetInstalledShvs

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetInstalledShvs viene** usato dall'agente protezione accesso alla rete per eseguire query sui validator dell'integrità del sistema installati nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Cambio\]
</dt> <dd>

Puntatore a un [valore SystemHealthEntityCount](nap-datatypes.md) che specifica il numero di SHV installati negli *ID*.

</dd> <dt>

*ID* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di [valori SystemHealthEntityId](nap-datatypes.md) che contengono gli ID SHV installati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                   | Descrizione                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione riuscita.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Al metodo è stato passato un argomento non valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





