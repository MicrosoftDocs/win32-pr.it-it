---
title: Metodo GetExportPath della Win32_RDMSDeploymentSettings classe
description: Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Metodo GetExportPath Servizi Desktop remoto
- Metodo GetExportPath Servizi Desktop remoto , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Servizi Desktop remoto metodo , GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b77db7a72ff91ee4c161f847f5021cc4dcfe1ad8ee46d08fb8b67be1f341850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080121"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetExportPath della classe \_ WIN32 RDMSDeploymentSettings

Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ Cambio\]
</dt> <dd>

Riceve il percorso della directory.

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

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





