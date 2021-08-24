---
title: Metodo GetClientAccessName della classe Win32_RDMSEnvironment
description: Recupera il nome Domain Name System record di risorse DNS (RR) dell'ambiente Desktop remoto Management Services (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Metodo GetClientAccessName Servizi Desktop remoto
- Metodo GetClientAccessName Servizi Desktop remoto , Win32_RDMSEnvironment classe
- Win32_RDMSEnvironment classe Servizi Desktop remoto metodo , GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 206ef89765bd18a73559c98d70a614664d076099214bd20f7b97ca9c29e94bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139004"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Metodo GetClientAccessName della classe \_ RDMSEnvironment Win32

Recupera il nome Domain Name System record di risorse DNS (RR) dell'ambiente Desktop remoto Management Services (RDMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientAccessName* \[ Cambio\]
</dt> <dd>

Riceve il nome RR recuperato.

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

 

 





