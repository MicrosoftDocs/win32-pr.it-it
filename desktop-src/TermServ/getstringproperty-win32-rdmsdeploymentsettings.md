---
title: Metodo GetStringProperty della classe Win32_RDMSDeploymentSettings
description: Recupera una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400458"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetStringProperty della \_ classe RDMSDeploymentSettings Win32

Recupera una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Alias dell'insieme di desktop virtuali.

</dd> <dt>

*Valore* \[ di out\]
</dt> <dd>

Stringa che riceve il valore recuperato.

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

 

 





