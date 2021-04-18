---
title: Metodo GetClientAccessName della classe Win32_RDMSEnvironment
description: Recupera il nome del record di risorse Domain Name System (DNS) dell'ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetClientAccessName
- Metodo GetClientAccessName Servizi Desktop remoto, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, metodo GetClientAccessName
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
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301119"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Metodo GetClientAccessName della \_ classe RDMSEnvironment Win32

Recupera il nome del record di risorse Domain Name System (DNS) dell'ambiente Desktop remoto Management Services (RDBMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientAccessName* \[ out\]
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
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSEnvironment Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





