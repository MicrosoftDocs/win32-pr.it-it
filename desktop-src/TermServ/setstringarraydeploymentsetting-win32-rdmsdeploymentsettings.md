---
title: Metodo SetStringArrayDeploymentSetting della classe Win32_RDMSDeploymentSettings
description: Aggiorna le impostazioni di distribuzione per un insieme di desktop virtuali.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetStringArrayDeploymentSetting
- Metodo SetStringArrayDeploymentSetting Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743490"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo SetStringArrayDeploymentSetting della \_ classe RDMSDeploymentSettings Win32

Aggiorna le impostazioni di distribuzione per un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Alias dell'insieme di desktop virtuali.

</dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Matrice di stringhe che contiene le nuove impostazioni di distribuzione.

</dd> </dl>

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

 

 





