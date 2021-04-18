---
title: Metodo GetInt32Property della classe Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Recupera una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetInt32Property
- Metodo GetInt32Property Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301901"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetInt32Property della \_ classe RDMSDeploymentSettings Win32

Recupera una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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

Intero che riceve il valore recuperato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSDeploymentSettings Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





