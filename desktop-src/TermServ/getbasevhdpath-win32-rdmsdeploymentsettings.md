---
title: Metodo GetBaseVHDPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali. | Metodo GetBaseVHDPath della classe Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetBaseVHDPath
- Metodo GetBaseVHDPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969153"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetBaseVHDPath della \_ classe RDMSDeploymentSettings Win32

Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Riceve il percorso di distribuzione del disco rigido virtuale.

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

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





