---
title: Metodo GetActiveServer della classe Win32_RDMSEnvironment
description: Recupera il nome di dominio completo (FQDN) dell'ambiente Desktop remoto Management Services (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Metodo GetActiveServer Servizi Desktop remoto
- Metodo GetActiveServer Servizi Desktop remoto , Win32_RDMSEnvironment classe
- Win32_RDMSEnvironment classe Servizi Desktop remoto metodo , GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730fa1230ddf08f5bd598e2041cd82ab4287d30387fa61460771fea5bcf3ec50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139014"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Metodo GetActiveServer della classe \_ RDMSEnvironment Win32

Recupera il nome di dominio completo (FQDN) dell'ambiente Desktop remoto Management Services (RDMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NomeServer* \[ Cambio\]
</dt> <dd>

Riceve il nome di dominio completo recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSEnvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





