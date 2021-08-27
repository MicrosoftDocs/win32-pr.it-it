---
title: Metodo GetDiffVHDPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per una raccolta di desktop virtuali.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Metodo GetDiffVHDPath Servizi Desktop remoto
- Metodo GetDiffVHDPath Servizi Desktop remoto , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Servizi Desktop remoto metodo , GetDiffVHDPath
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
ms.openlocfilehash: ad8783d20737c98dcccf769924ea1544c21dec8ffa3ff340aa285be163b8925b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099541"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetDiffVHDPath della classe \_ RDMSDeploymentSettings Win32

Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per una raccolta di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ Cambio\]
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
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





