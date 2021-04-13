---
title: Metodo GetDiffVHDPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetDiffVHDPath
- Metodo GetDiffVHDPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400322"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetDiffVHDPath della \_ classe RDMSDeploymentSettings Win32

Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ out\]
</dt> <dd>

Riceve il nuovo percorso del disco differenze.

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

 

 





