---
title: Metodo SetClientAccessName della classe Win32_RDMSEnvironment
description: Aggiorna il nome del record di risorse Domain Name System (DNS) di un ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetClientAccessName
- Metodo SetClientAccessName Servizi Desktop remoto, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, metodo SetClientAccessName
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
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302596"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Metodo SetClientAccessName della \_ classe RDMSEnvironment Win32

Aggiorna il nome del record di risorse Domain Name System (DNS) di un ambiente Desktop remoto Management Services (RDBMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientAccessName* \[ in\]
</dt> <dd>

Nome del nuovo RR.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSEnvironment Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





