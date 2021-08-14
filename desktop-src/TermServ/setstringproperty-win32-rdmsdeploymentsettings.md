---
title: Metodo SetStringProperty della Win32_RDMSDeploymentSettings classe (Certenroll.h)
description: Aggiorna una proprietà stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Metodo SetStringProperty Servizi Desktop remoto
- Metodo SetStringProperty Servizi Desktop remoto , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Servizi Desktop remoto, metodo SetStringProperty
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
ms.openlocfilehash: 1001d5c723642357263a6029c3569eaa861f7dcf3689cc7d06b42e04ef461aa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987501"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo SetStringProperty della classe \_ RDMSDeploymentSettings Win32

Aggiorna una proprietà stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Alias dell'insieme di desktop virtuali.

</dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Nuovo valore della proprietà.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





