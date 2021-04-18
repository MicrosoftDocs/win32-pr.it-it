---
title: Metodo SetInt32Property della classe Win32_RDMSDeploymentSettings
description: Aggiorna una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302448"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo SetInt32Property della \_ classe RDMSDeploymentSettings Win32

Aggiorna una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
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
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





