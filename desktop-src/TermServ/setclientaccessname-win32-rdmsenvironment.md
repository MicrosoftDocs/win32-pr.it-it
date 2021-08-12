---
title: Metodo SetClientAccessName della classe Win32_RDMSEnvironment
description: Aggiorna il Domain Name System di risorse DNS (Dns) di un ambiente Desktop remoto Management Services (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Metodo SetClientAccessName Servizi Desktop remoto
- Metodo SetClientAccessName Servizi Desktop remoto , Win32_RDMSEnvironment classe
- Win32_RDMSEnvironment classe Servizi Desktop remoto, metodo SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb962a6dd1600ad0cd439f7f34772f69d91b925308e2247e1283575d8f68cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604873"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Metodo SetClientAccessName della classe \_ RDMSEnvironment Win32

Aggiorna il Domain Name System di risorse DNS (Dns) di un ambiente Desktop remoto Management Services (RDMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientAccessName* \[ Pollici\]
</dt> <dd>

Nuovo nome RR.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSEnvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





