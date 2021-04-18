---
title: Metodo GetExportPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetExportPath
- Metodo GetExportPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetExportPath
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
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301117"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetExportPath della \_ classe RDMSDeploymentSettings Win32

Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Riceve il percorso della directory.

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

 

 





