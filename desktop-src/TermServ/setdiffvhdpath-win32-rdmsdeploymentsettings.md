---
title: Metodo SetDiffVHDPath della Win32_RDMSDeploymentSettings classe
description: Aggiorna il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Metodo SetDiffVHDPath Servizi Desktop remoto
- Metodo SetDiffVHDPath Servizi Desktop remoto , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Servizi Desktop remoto , metodo SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d275f848bb29c9cac4930f738a9a123cc6aa3a8e80a77b746f2495d44f68cf96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988041"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo SetDiffVHDPath della classe \_ WIN32 RDMSDeploymentSettings

Aggiorna il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryPath* \[ Pollici\]
</dt> <dd>

Nuovo percorso del disco differenze.

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

 

 





