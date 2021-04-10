---
title: Metodo SetSMBPath della classe Win32_RDMSDeploymentSettings
description: Aggiorna il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSMBPath
- Metodo SetSMBPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964500"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo SetSMBPath della \_ classe RDMSDeploymentSettings Win32

Aggiorna il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ in\]
</dt> <dd>

Nuovo percorso della condivisione SMB, in formato UNC.

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

 

 





