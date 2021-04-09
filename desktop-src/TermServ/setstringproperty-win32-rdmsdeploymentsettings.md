---
title: Metodo SetStringProperty della classe Win32_RDMSDeploymentSettings (CertEnroll. h)
description: Aggiorna una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo SetStringProperty
- Metodo SetStringProperty Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, Metodo SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120387"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo SetStringProperty della \_ classe RDMSDeploymentSettings Win32

Aggiorna una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
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

Nuovo valore della proprietà.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>CertEnroll. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





