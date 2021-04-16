---
title: Metodo INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Utilizzato dall'agente NAP per eseguire una query sui validator di integrità di sistema installati (SHV) nel client.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- NAP metodo GetInstalledShvs
- Metodo GetInstalledShvs NAP, interfaccia INapEnforcementClientConnection2
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
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479355"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>Metodo INapEnforcementClientConnection2:: GetInstalledShvs

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetInstalledShvs** viene utilizzato dall'agente NAP per eseguire una query sui validator di integrità del sistema installati (SHV) nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di out\]
</dt> <dd>

Puntatore a un valore [SystemHealthEntityCount](nap-datatypes.md) che specifica il numero di SHV installati negli *ID*.

</dd> <dt>

*ID* \[ di out\]
</dt> <dd>

Puntatore a una matrice di valori [SystemHealthEntityId](nap-datatypes.md) che contengono gli ID di convalida integrità di sistema installati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                   | Descrizione                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione riuscita.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un argomento non valido è stato passato al metodo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





